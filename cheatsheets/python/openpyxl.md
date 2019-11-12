# openpyxl (Python module) Cheatsheet

Files & Sheets
- Import openpyxl
- wb = openpyxl.load_workbook("file_name.xlsx")
- Print(wb.sheetnames)
- Sheet = wb["Sheet1"]
- Wb.create_sheet("Sheet2", 0)
- Wb.remove_sheet(sheet)
- Sheet.max_row
- Sheet.max_column
- Sheet.append([1,2,3])
- Sheet.delete_rows/cols
- Wb.save("new_file_name.xlsx")

## Worksheet
- ws.max_column
- ws.max_row

### Cells
#### Access
- ws.cell(row=y, col=x)
- Cell = ws["a1"]
- ws["a"] - all cells in "a" column
- ws["a:c"]
- ws["a1:c3"]
- ws[1:3]
- cell.value
#### Attributes
- cell.row
- cell.column
- cell.coordinate

Cell Coordinates
- Cell = Sheet.cell(1,10) = "XYZ"
- Cell = Sheet.cell(row=1, column=1) = 345
	
Loop through cells
- For row in range(1, sheet.max_row+1):
	- do stuff
- Cell = sheet.cell(row, column)
