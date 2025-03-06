---
{"dg-publish":true,"permalink":"/linked-files/virtual-voids/"}
---

```
class Instrument{
	public:
	virtual void makeSound(){
		cout << "the instrument is playing" <<endl;
	}

	//virtual void makeSound() = 0;
	
	This class, by merit of having at least one pure virtual function has   become an abstract class.
	
};

class Accordion :public Instrument{ //Accordion is a derived class
public:
	void makeSound(){ // more derived than the one in base class (duh)
		cout << "an accordian is playing" <<endl;
	}
};

class Piano :public Instrument{ //Accordion is a derived class
public:
	// no overrider. this will cause an error if we had a PVF in our base function.
};


int main()
{
	Intrument* i1 = new Accordion();
	i1 -> makeSound();   // -> is dot for pointers
	
	Intrument* i2 = new Piano();
	i2 -> makeSound();   // error will occur if a pure virtual function has no overrider in the derived class

	Instrument* instruments[2] = {i1,i2};
	for(use for range loop){
		intruments[i] -> makeSound(); 
		// this will make sound for piano and accordian
	}
	
```