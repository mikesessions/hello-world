# hello-world

#include <iostream>
#include <string>

using namespace std;

unsigned long getnum(void);

int main()
{
    
    unsigned long mynumber;
    
  string name;
  /*
  std::cout << "What is your name? ";
  getline (std::cin, name);
  std::cout << "Hello, " << name << "!\n";
  */
  cout << "Enter a valid number: ";
  if(mynumber = getnum())
    {cout << endl << mynumber;}
  else 
   {
  cout << "Invalid number";
   }
}


long getnum(void)
{
        char buffer[80];
        char* pbuffer=buffer;
        cin.getline(buffer,80);
        
        while(1)
        {
            if(*pbuffer >= 48 && *pbuffer <=57)  //asci value range for numbers 0-9
            
                pbuffer++;
                
            else if(*pbuffer==0 && (buffer[0]>=48 & buffer[0]<=75))
                {
                    return atol(buffer,NULL,10);  //end of input. true number found
                    
                }
            else 
                {
                    return false;
                }// we've found a false number
                
        }   
}            
    
long getnum(void)

{
       
 
char buffer[80];
        
 char* pbuffer=buffer;
        
 cin.getline(buffer,80);
 
    while(1)
       
      {
            
	if(*pbuffer >= 48 && *pbuffer <=57)  //asci value range for numbers 0-9
            
              
           pbuffer++;
                
           
        else if(*pbuffer==0 && (buffer[0]>=48 & buffer[0]<=75))
            
          {
                   
              return atol(buffer);  //end of input. true number found

          }
                
            
        else 
                
          {
                   
              return EOF;
               
          }// we've found a false number
          
      }  

}  
