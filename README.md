# UE4-IOS-IPV6
# Problem
AppStore require every app support ipv6, when I develop a .io game, my agame reject by apple,
the reason is the game is not support ipv6, it will stay on loading screen when they test under ipv6.

I google and found almost no one give an answer, So I read the engine code, and finaly fix it, I test 
the game in my dns64/nat64 env.

So I share the code for every one who have the same problem:
your game connect the dedicated server on the remote, and by default, you can not connect under ipv6.

I test on Unreal Engine 4 4.18.2


# How to use it

1. you must have an cpp project, if you are use a blueprint project, see [the video](https://youtu.be/DRtkq0ewTz4) to convert to a 
cpp project.

2. copy the two file to your game source path:ProjectRoot/Source/YourGame/
   please remember change the YourGame to your own game name.

3. edit the Config/DefaultEngine.ini, add content:

  [/Script/OnlineSubsystemUtils.IpNetDriver]
NetConnectionClassName=/Script/YourGame.TankIpConnection

4. build the game, launch on the iphone or ipad device.


If you have any question, feel free to email me:feixuwu@outlook.com
