# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types.


## AIM:
To implement the Abstract Factory Design Pattern in Java by creating UI components (Buttons and Checkboxes) for two different themes—Dark and Light.
Based on user input, the appropriate factory should generate the correct themed UI elements.
## ALGORITHM :


<img width="561" height="779" alt="image" src="https://github.com/user-attachments/assets/183596ca-408f-4ceb-9c56-bd2b706f08bd" />







## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: POPURI SRAVANI
RegisterNumber:212223240117  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button
{ 
    void render();
}
interface Checkbox 
{ 
    void render();
}

class DarkButton implements Button 
{
    public void render()
    { 
        System.out.println("Dark Button created"); 
    }
}

class LightButton implements Button 
{
    public void render() 
    {
        System.out.println("Light Button created"); 
    }
}

class DarkCheckbox implements Checkbox
{
    public void render() 
    { 
        System.out.println("Dark Checkbox created"); 
    }
}

class LightCheckbox implements Checkbox
{
    public void render() 
    { 
        System.out.println("Light Checkbox created");
    }
}

interface UIFactory 
{
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new DarkButton(); 
    }
    public Checkbox createCheckbox() 
    { 
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory 
{
    public Button createButton() 
    {
        return new LightButton();
    }
    public Checkbox createCheckbox() 
    {
        return new LightCheckbox(); 
    }
}

public class Main 
{
    public static void main(String[] args)
    {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else
        {
            System.out.println("Invalid theme");
            return;
        }
        factory.createButton().render();
        factory.createCheckbox().render();
    }
}
```







## OUTPUT:

<img width="808" height="341" alt="image" src="https://github.com/user-attachments/assets/661a04b0-0895-4f95-932f-b78896a38ac1" />




## RESULT:
The program successfully demonstrates the Abstract Factory Pattern by creating theme-specific UI components.
Based on user input, the correct factory is selected, and it generates:
A Dark Button and Dark Checkbox or
A Light Button and Light Checkbox
Both components are rendered in the output according to the selected theme.

