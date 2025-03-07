---
{"dg-publish":true,"permalink":"/linked-files/virtual-destructor/"}
---

virtual destructors allow us to destruct derived classes with a pointer to the base class. 


```
/**
 * \file
 * \author Junseok Lee
 * \date 2025 Spring
 * \par cs170s25.kr High Level Programming II
 * \copyright DigiPen Institute of Technology
 */

// TODO define IUpdate abstract interface class/struct

class IUpdate 
{
    public:
    
    virtual void Update(double delta_time) = 0;

    virtual ~IUpdate()= default; 
    //shut down logic for the class is default (do nothing)
    
};
```