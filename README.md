# LTHMonthYearPickerView
Simple to use month & year picker view for those pesky Credit Card expiration dates & Co.

# How to use
Drag the contents of `LTHMonthYearPickerView` to your project, or add `pod 'LTHMonthYearPickerView'` to your podspec file.

```objc
/*
 @numberedMonths: set to YES if you want months to be returned as 01, 02, etc.
 @shortMonths: set to YES if you want months to be returned as Jan, Feb, etc.
 @shortMonths: set to NO if you want months to be returned as January, February, etc.
 @date: set it if you want the picker to be initialized with a specific month and year;
	it automatically fetches the month & year from @date.
 @showToolbar: set to YES if you want the picker to have a Cancel & Done toolbar.
 */
_monthYearPicker = [[LTHMonthYearPickerView alloc] initWithDate: [NSDate date]
													shortMonths: NO
												 numberedMonths: NO
													 andToolbar: YES];
_monthYearPicker.delegate = self;
```

Comes with 3 delegate methods:
```objc
- (void)pickerDidSelectRow:(NSInteger)row inComponent:(NSInteger)component;
- (void)pickerDidPressDoneWithMonth:(NSString *)month andYear:(NSString *)year;
- (void)pickerDidPressCancel;
// Or corresponding notifications; if you prefer it like that, just uncomment the notification posts.
```

That's it.

Everything is easily customizable with macros and constants, from month & year fonts and colors (individually) to the month names, if you need them in another language.

![Screenshot](http://rolandleth.com/assets/monthyearpickerview/Screenshot.png)

# Apps using this control
If you're using this control, I'd love hearing from you! 

# License
Licensed under MIT. If you'd like (or need) a license without attribution, don't hesitate to [contact me](mailto:roland@rolandleth.com).