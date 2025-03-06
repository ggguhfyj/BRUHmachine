---
{"dg-publish":true,"permalink":"/linked-files/inheritance-and-derived-classes/"}
---


"YouTubeChannel" base class has 4 properties, a constructor and a public function.

```
class CLASSNAME : public YouTubeChannel {
public:
	CLASSNAME (string name, string ownerName): Youtubechannel(name,ownername) {
	
	}
	void Practice()
	{
		cout << "something" << endl;
		
	}
};
```

- The Derived Class can access the PUBLIC and PROTECTED members of the base class but not the other way around.
- Constructors are not inherited when creating a derived class. 


```
int main()
{
	CLASSNAME classobject("name","name2");
	
}
```