### CPP CHECKER -- missed command
`cppcheck ... `



### CLANG CHECKER 
`scan-build make`



### googletest

```
TEST(Name of test set, Name of subset for tests)
{

  create obj (param1,2,3)

  EXPECT_EQ(obj.func1,param1);

}
TEST(ValidPackets, goodCode){
  

}
main(int argc, char** argv)
{
  ::testing::InitGoogleTest(&argc,argv);
  return RUN_ALL_TESTS();

} 
```
