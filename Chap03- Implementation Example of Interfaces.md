## Implementation Using Interface

In our game, we are using **multiple inheritances** using interfaces for the damage and shooting system in our project. For this, first, we have to create an interface called IDamagable & IShootable. But remember if you are making an interface, always the name of that interface will start with I then followed by any name like - IShootable, IDamagable, etc.

Like this -
```C#
public interface IDamagable
    {
      void applyDamage(float damage);
      int currentHealth{get;}
    }
```

```C#
public interface IShootable
  {
    void shootBullets(int bullets);
    int weapon{get;}
  }
```

While declaring the aboev 2 interaces, we can note that Interface members don't have access modifiers, as they are all **public**.

---
In order to use interfaces in empty/child classes, you have to inherit the interface first and then implement all the methods which are inside it. Each class that implements the interface will have its own methods or properties body. 

Like this -
```C#
public class EnemyView: Monobehaviour, IDamagable, IShootable
	 {
	    public void TakeDamage(float damage)
            public void TakeBullets(int bullets)
	    
      	   {
             controller.ApplyDamage(damage);
           }
        
           {
             controller.shootBullets(bullets);
           } 
	   
	 };
```
EnemyController -
```C#
public class EnemyController
	 {
 	    public void ApplyDamage(float damage)
           {
              if (model.health <= 0) return;
              if (model.health - damage <= 0)
              {
                  //enemy dead
              }
               else
              {         
                 model.health -= damage;
              }
        
           public void shootBullets(int bullets)
          {
             //Fire bullet
          }
	  
	 };
```
