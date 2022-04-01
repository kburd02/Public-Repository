# Public-Repository
Available for recruiters, instructors, peers
#include <stdio.h>
#include <iostream>

using namespace std;

template <class elemType>
void bubbleSort (elemType list[], int length)
{
	int measure = 0;
	bool isSorted=false; 
    
    for (int iteration =1; (iteration < length) && !isSorted;
	 iteration++) //4operations
	 
    {	measure=measure+4;
    	isSorted =true;
    	
        for (int index=0; index< length-iteration; index++)//4 operations   
        {
        	 measure=measure+4;
            if (list[index] > list[index +1])//2 operations
            {
                elemType temp = list[index];//1 operation
                list[index] = list[index + 1];// 2 operations
                list[index+1] = temp;// 2 operations
                isSorted= false;//1 operation
                //measure = measure + 5; 
                measure =measure+6;
                
            }//a max of 16 ;min would be  
        }
        measure = measure + 2;
        
    }
    cout<< "The number of calculations done are" <<" "<< measure <<endl; 
}
//add lines to calaculate the number of calcultaions performed
//measure the amount tp operations performed
//keep a copy of the list for part 25...randomly generated or put them a file and read them into the program
// remeber the order of the numbers that will be inserted
//can randomly generate it
//submit program and cpp
//fill in what is in the chart
//opration can be an assignment,comparison, 
// in essence determine how many time an assignment is made and a comparison is formed and increment

template<class elemType> 
void print (elemType list[], int length);
int main()
//measure

{
    int intList[] = {43,1,22,33,64,49,31,5,12,71};
    cout << "Before sorting the list of 10, the list is: \n";
    print (intList, 10);
    cout<<endl;
    bubbleSort(intList,10);
    cout<< "After sorting the list of 10, the list is: \n";
    print (intList,10);
    cout<<"\n";


 //list of 30
    int intList2[] = {20,14,61,28,127,65,7,97,99,60,138,8,33,87,68,19,39,55,59,36,94,82,23,38,134,26,12,41,106,122};
    cout <<"Before sorting the list of 30, the list is: \n";
    print (intList2, 30);
    cout<<endl;
    bubbleSort(intList2,30);
    cout<< "After sorting the list of 30, the list is: \n";
    print (intList2,30);
    cout<<"\n";
    
//list of 50
	int intList3[] = {42,5,177,199,248,207,135,152,179,25,100,3,48,22,6,83,87,150,201,249,138,167,90,128,146,142,110,172,12,181,115,9,118,227,2,244,10,72,144,34,124,94,237,231,157,53,41,98,11,52};
    cout <<"Before sorting the list of 50, the list is: \n";
    print (intList3, 50);
    cout<<endl;
    bubbleSort(intList3,50);
    cout<< "After sorting the list of 50, the list is: \n";
    print (intList3,50);
    cout<<"\n";
        
//list of 70
    int intList4[] = {79,226,288,116,185,69,353,270,376,101,208,1,112,60,217,72,367,305,394,104,238,256,347,324,109,332,107,246,187,73,250,286,17,245,40,62,16,129,373,195,157,348,310,254,326,357,121,191,152,209,176,7,30,100,201,260,123,145,46,395,78,265,304,84,361,99,92,49,67,110};
    cout <<"Before sorting the list of 70, the list is: \n";
    print (intList4, 70);
    cout<<endl;
    bubbleSort(intList4,70);
    cout<< "After sorting the list of 70, the list is: \n";
    print (intList4,70);
    cout<<"\n";
 //list of 100  
    int intList5[] = {328,682,543,240,600,598,735,633,354,222,179,229,140,599,319,454,56,539,16,232,536,546,202,570,681,82,221,341,130,286,542,670,478,175,654,187,106,780,477,4,199,705,606,632,323,168,406,408,373,261,178,457,217,676,33,511,514,383,207,520,662,750,74,777,584,487,188,47,784,143,455,764,650,201,404,660,361,241,374,449,566,326,24,381,193,206,262,46,109,52,331,367,613,700,192,537,13,266,257,403};
    cout <<"Before sorting the list of 100, the list is: \n";
    print (intList5, 100);
    cout<<endl;
    bubbleSort(intList5,100);
    cout<< "After sorting the list of 100, the list is: \n";
    print (intList5,100);
    return 0;
    
    
}

template <class elemType>
void print (elemType list[], int length)
{
	for(int i=0; i <length; i++)
	cout <<list[i]<<" ";
	cout <<endl;
}
