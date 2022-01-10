## Problem

We want to verify that a file is downloaded with the right data as a result of user interaction.  
Unfortunately, file download isn't supported in jest so we need to mock some stuff to see that the data is constructed properly.

## Solution

We mock the `createObjectURL` on the window to verify that when it's called, it contains the data we want to export.  
The rest of the download process is only clicking on the `a` element to trigger the download so this isn't covered here.

```jsx
it('Exports to CSV', async () => {
  const createObjectURLMock = jest.fn((url) => url);
  Object.defineProperty(window.URL, 'createObjectURL', { value: createObjectURLMock });
  render(<PageWithExportFunctionalioty />);

  userEvent.click(screen.getByRole('button', { name: /export to csv/i }));

  // Since we can't really verify file download, we verify that the URL object
  // is being defined properly because the download process is defined in the export-to-csv package.
  expect(await new Response(createObjectURLMock.mock.calls[0][0]).text()).toMatchInlineSnapshot(`The snaphost of your data`);
});
```
