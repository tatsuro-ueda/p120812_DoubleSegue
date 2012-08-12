I tried to move segue continually, but I failed, too.

So I tried to set interval between first segue and second segue for one second.

![ss](http://farm8.staticflickr.com/7260/7763459050_1592827bbb_o.png)

This works well ! When you push button in red window, green window appears, and after it, blue window appears automatically.

	- (void)viewDidLoad
	{
	    [super viewDidLoad];
		// Do any additional setup after loading the view, typically from a nib.
	    [self performSelector:@selector(segue) withObject:nil afterDelay:1.0];
	}
	
	- (void)segue
	{
	    [self performSegueWithIdentifier:@"toBlue" sender:self];
	}