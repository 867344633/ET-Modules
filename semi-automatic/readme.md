# ���Զ�����ET����˿�����
## ��Է������˵���ع��򣬶Է���˵Ŀ�������һ���̶ȵĳ���ʵ�ְ��Զ����Ŀ�������߿���Ч�ʣ�ʵ�֡�����һ������ˡ���Ŀ�ꡣ
### �����ǰ����ǹ淶�����е����鶼Ҫ���ϸ�Ĺ淶������������Ĺ淶�������Ĺ淶�ȣ�ֻ�������м���ѭ����������°빦���ĳ��� Et�еķ���˿����������м���ѭ�ġ�ÿ�������������ɲ�ͬ�Ľ�����ɣ���ÿ�����������ɲ�ͬ������͹�����ɵģ��ɴˣ�һ�����ӻ��Ľṹ����������������

```
Server
    -����������
        -Event�¼�
        -Component ����������߼����
        -handler��������
```

### �����Ļ�����������һ��et����˵�ʱ���޷Ǿ�������Щevent��Component��handler����д���롣����һ�����Զ������ɶ�Ӧ��event��Component��handler�ṹ���ļ�������ǿ��Դ����߿���Ч�ʵġ�

## handler���������Զ����ɹ���˵��.
####  handler�ķ��ࣺ

```
����Et�ķ������ƣ�handler����Ϊ�������ࣺ
    AMhandler       ��ͨ��Ϣ������
    AMActorHandler  ��ͨRpc��Ϣ�Ĵ�����
    AActorHanler    ��ͨ��actor������
    AActorRpcHandler actorRpc������
    
    ���У�����rpc�����з���ֵ�ġ�
    
```

####  �淶

```
����Ҫ���ľ��Ǹ��������Լ���ҵ������ʹ������������hanler����������Ϣ�Ĵ���
��ʹ��������������ǰ������ж�Ӧ����Ϣ���ͣ�

ʹ�ð��Զ�handler����������ϢЭ��������淶��
    ��ͨ����Ϣ������_����������C2G_Login
    ��ͨRpc������Ϣ������_����������C2G_Login
    ��ͨRpc��Ӧ��Ϣ������_����������G2C_Login
    ��ͨActor��Ϣ����Actor_����_ʵ��_���� ���� Actor_C2G2M_Fight
    Actor ��Rpc��Ϣ����Actor_����_ʵ��_���� ���� Actor_C2G2M_Fight
    Actor��Rpc��Ϣ����Ӧ��Actor_����_ʵ��_���� ���� Actor_M2G2C_Fight
    
ʹ�ð��Զ�handler��������handler�������淶��
    Ҫ������Ϣ��+hanler.���� C2G_LoginHandler
    

```

####  ����˵��

```

��ѹ����õ������ļ���
AMActorRpcHandler.template  Actor��Rpc��Ϣ��������ģ��
AMessagehandler.template    ��ͨ����Ϣ��������ģ��
AMRpcHandler.template       ��ͨRpc��Ϣ�Ĵ�������ģ��
IActorHandler.template      ��ͨ��actor��������ģ��

gen                         ����һ���ļ��У����Ŀ¼

HandlerManifest.txt         Ҫ���ɵ�handler�б�����ƺõ�handler����д������ļ��С�
GenHandler.py               python�ű���ִ������ʼ����handler.cs�ļ���

```

####  ʹ������

1. ʹ��proto���ɹ���������ƺõ�Э���ļ���Э�������ѭ���������淶��
2. ��ƺ���Ҫ��Handler,��Handler���Ʒ��롾HandlerManifest.txt���ļ��С�
```
���磺
Actor_G2M_Unit_LogoutHandler
Actor_G2M_Room_ReconnectionHandler_RPC
G2M_CreateRoomHandler_RPC
G2M_EnterRoomHandler_RPC
G2M_GetCreatedRoomsHandler_RPC
Actor_C2G2M_Unit_LeaveRoomHandler_RPC
Actor_C2G2M_Unit_ReadyHandler_RPC
Actor_C2G2M_Unit_GetRoomInfoHandler_RPC
Actor_C2G2M_Unit_XiazhuHandler_RPC
Actor_C2G2M_Unit_KaipaiHanler_RPC
Actor_C2G2M_Unit_QiangzhuangHandler_RPC
Actor_C2G2M_Unit_TalkHandler
###### ע�⣡����������Ҫ�з���ֵ��RPC����Ϣ�Ĵ�����Ҫ��Handler�����_RPC���Ա�ǡ�
```

3. ִ��GenHandler.py 
4. ��gen�в鿴���ɵ��ļ���������Ŀ�У���΢�����ɡ�Ȼ��Ϳ�������Щhandler������Լ����߼�����