---
timezone: Asia/Dubai
---

# shiroshiro

1. I'm shiroshiro

2. No
   
## Notes

<!-- Content_START -->

### 2024.09.23

學習內容: 

1. finished 01 Hello Web3
2. deployed a contract on simulated EVM 
3. able to view the string from the contract
4. finished reading 02
5. understanding deploying contracts needs gas
6. finished 02 coding exercise


### 2024.09.24
1. 03 functions
2. pivate keyword => can be only accessed within this contract
3. extra solidity keywords => pure/view/payable
4. pure and view function doesnt cost gas ( no rewrite no gas fee )
5. low-level calls cost gas
6. internal and external functions
7. payable function for transferring eth
8. finished 03 quiz

### 2024.09.26

#### 04 function output
##### return
decalre return types => returns
normal return => return
returns can be named at the beginning of function => no return keyword needs at the end, still supports normal return tho

##### tuples
can contain different types of elements and be returned
syntax => (a,"b", [c,d,e])

#### 05 data storage and scope

##### reference type 
like pointers/address
can access same underlying data with different var like array/struct/mapping
##### data location
3 types: storage/memory/calldata, gas cost r different
storage: on chain like HDD/ high fee
memory: in mem
calldata: in mem but cant modify, usually used in param
##### modifying reference data
pointing uint[] x = [1,2,3]; // state variable: array x
then assign uint[] storage xStorage = x; xStorage[0] = 100; 
will modify x => [100,2,3]

##### variable scope
state var: on chain/ high gas, declared outside of the function
    can change state var in functions
local var: only avalible in func like normal, low gas
global var: reserved keywords for solidity　like blcok hash etc.
    

### 2024.09.27

#### 06 array and struct
fixed or dynamic size array
fixed decalre: type[length] name
dynamic decalre: type[] name / bytes name
bytes is cheaper than bytes1[]

#### array
memory dynamic array:  uint[] memory array8 = new uint[](5);
    bytes memory array9 = new bytes(9);
array literals first element must hv type/ type with the smallest storage space is used by default

array methods length/push()/push(x)/pop()

#### struct
just like normal old struct nothing special

### 2024.09.29

#### mapping

can be quered by key like normal mapping

### 2024.10.01

#### mapping rules

keytype must be default types of solidity => no struct
but value type can be anything

must be storage but cant be used in return result of public func

if mapping is public,  a getter function will be created auto for quering value by key

adding mapping pair by _Var[_Key] = _Value

### 2024.10.02

#### principle of mapping

doesnt store key or length info
uses keccak256(key) as offset ?

#### 08 initla value

getter func => var()
deleting a var will reset it to default

### 2024.10.03

#### why mapping?
efficient memory space and fast access
like hash tables

### 2024.10.05

#### control flow
just like normal control 
if/else/for/while/do/ternary

uint sortting trap, notice dont let uint gets negative

### 2024.10.06

#### constructor

runs when contract deploys
used to init params eg owner addr

syntax not consistent for solidity ver

#### modifier 
used to declare dedicated properties of functions
sually used for restrict access => require(msg.sender == owner)


<!-- Content_END -->
