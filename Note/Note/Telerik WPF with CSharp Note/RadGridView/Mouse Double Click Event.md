Mouse Double Click 事件註冊
`gridView.MouseDoubleClick += GridView_MouseDoubleClick;`

Mouse Double Click Cell
```
private void GridView_MouseDoubleClick(object sender, MouseButtonEventArgs e)
{
	
	FrameworkElement originalSender = e.OriginalSource as FrameworkElement;
	if (originalSender != null)
	{
		//var cell = originalSender.ParentOfType<GridViewCell>();
		//if (cell != null)
		//{
		//    MessageBox.Show("The double-clicked cell is " + cell.Value);
		//}
		
		//var row = originalSender.ParentOfType<GridViewRow>();
		var cell = originalSender.ParentOfType<GridViewCell>();

		if(cell != null && cell.Column.UniqueName == "Name")
		{
			Unsubscript();
			var pinName = ((Pin)cell.DataContext).Name;
			if(textBox.ContainsPinName(pinName))
			{
				textBox.RemovePinNames(pinName);
			}
			else
			{
				textBox.AddPinNames(pinName);
			}
			SyncGridView();
			Subscript();
		}
		
	}
	
}
```