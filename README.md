# 📝 Tutorial & Exercise 10 📝

**Student Details:**

| Attribute | Information                |
|-----------|----------------------------|
| Name      | Andika Pramudya Wardana   |
| Student ID| 2206046645                 |
| Class     | Advanced Programming KKI   |

---

<details>
<summary>Module 10: High-Level Networking</summary>

## Questions and Answers

### -> Reflection

#### 1.2: Understanding how it works
**Result:** 
```rust 
PS C:\Users\Dika\timer_future> cargo run
   Compiling timer_future v0.1.0 (C:\Users\Dika\timer_future)
    Finished dev [unoptimized + debuginfo] target(s) in 1.29s
     Running `target\debug\timer_future.exe`
Andika Computer: Hey heyy!
Andika's Computer: howdy!
Andika's Computer: done!
```


    When I spawn a task using the provided spawner, it initiates an asynchronous process that prints "Andika's Computer: howdy!", then waits for 2 seconds before printing "Andika's Computer: done!". However, before the execution of this task, I insert a synchronous println!("Andika Computer: Hey heyy!"); statement in the main function. Consequently, when the program runs, the synchronous println! statement executes immediately, printing "Andika Computer: Hey heyy!", while the asynchronous task spawned earlier executes subsequently, printing "Andika's Computer: howdy!" after 2 seconds of waiting, followed by "Andika's Computer: done!".

#### 1.3: Multiple Spawn and removing drop
**Result:** 
```rust 
PS C:\Users\Dika\timer_future> cargo run
    Compiling timer_future v0.1.0       
     (C:\Users\Dika\timer_future)
        Finished dev [unoptimized + debuginfo]  
         target(s) in 0.91s
        Running `target\debug\timer_future.exe`
    Andika Computer: Hey heyy!
    Andika's Computer: howdy!
    Andika's Computer: howdy!
    Andika's Computer: howdy!
    Andika's Computer: done!
    Andika's Computer: done!
    Andika's Computer: done!
```


    
    When multiple tasks are spawned asynchronously  
    using the spawner, each task prints "Andika's 
    Computer: howdy!", then waits for 2 seconds before 
    printing "Andika's Computer: done!". Concurrently, 
    a synchronous println!("Andika Computer: Hey heyy!"); statement executes immediately. Upon running the program, the synchronous print statement executes first, printing "Andika Computer: Hey heyy!", followed by the concurrent execution of the three asynchronous tasks, each printing "Andika's Computer: howdy!" one after another. Subsequently, each task waits for 2 seconds before printing "Andika's Computer: done!". Therefore, the output consists of "Andika Computer: Hey heyy!", followed by three sets of "Andika's Computer: howdy!" and three sets of "Andika's Computer: done!".

---

</details>