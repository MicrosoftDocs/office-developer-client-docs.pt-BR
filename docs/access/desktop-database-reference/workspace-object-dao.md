---
title: Objeto Workspace (DAO)
TOCTitle: Workspace Object
ms:assetid: bf3ab863-5e9a-4842-1f82-2ccf958d9779
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822782(v=office.15)
ms:contentKeyID: 48547481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 2c734d5e0f022faec4ebb9efe2dfc2f7dd7b7979
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711578"
---
# <a name="workspace-object-dao"></a>Objeto Workspace (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Um objeto **Workspace** define uma sessão nomeada por um usuário. Ele contém bancos de dados abertos e fornece mecanismos para transações simultâneas e, nos espaços de trabalho do Microsoft Access, suporte a grupos de trabalho seguros.

## <a name="remarks"></a>Comentários

Um **Workspace** é um objeto não persistente que define como o aplicativo interage com os dados  utilizando o mecanismo de banco de dados do Microsoft Access ou o ODBCDirect. Use o objeto **Workspace** para gerenciar a sessão atual ou para iniciar uma sessão adicional. Em uma sessão, você pode abrir vários bancos de dados ou conexões e gerenciar transações. Por exemplo, você pode:

- Usar as propriedades **Name**, **UserName** e **Type** para estabelecer uma sessão chamada. A sessão cria um escopo no qual é possível abrir vários bancos de dados e realizar uma instância de transações aninhadas.

- Usar o método **Close** para encerrar uma sessão.

- Usar o método **OpenDatabase** para abrir um ou mais bancos de dados existentes em um **Workspace**.

- Usar os métodos **BeginTrans**, **CommitTrans** e **Rollback** para gerenciar o processamento de transações aninhadas dentro de um **Workspace** e usar vários objetos **Workspace** para realizar diversas operações simultâneas e de sobreposição.

Quando você primeiro consultar ou usa um objeto **Workspace** , você cria o espaço de trabalho padrão, DBEngine.Workspaces(0) automaticamente. As configurações das propriedades **nome** e **nome de usuário** do espaço de trabalho padrão são "\#espaço de trabalho padrão\#" e "Admin", respectivamente. Se a segurança estiver ativada, a configuração da propriedade **UserName** é o nome do usuário que fez logon.

Quando você utiliza transações, todos os bancos de dados no **Workspace** especificado são afetados  mesmo se vários objetos **Database** forem abertos no **Workspace**. Por exemplo, você usa um método **BeginTrans**, atualiza vários registros em um banco de dados e, em seguida, exclui registros de outro banco de dados. Se você utilizar o método **Rollback**, as operações de atualização e exclusão serão canceladas e revertidas. Você pode criar objetos **Workspace** adicionais para gerenciar transações, de forma independente, nos objetos **Database**.

É possível criar objetos **Workspace** com o método **CreateWorkspace**. Depois de criar um novo objeto **Workspace**, você deve acrescentá-lo à coleção **Workspaces** se precisar se referir a ela a partir da coleção **Workspaces**.

Você pode usar um objeto **Workspace** recém-criado sem acrescentá-lo à coleção **Workspaces**. Entretanto, você deve se referir a ele pela variável de objeto que foi atribuída a ele.

Para referir-se a um objeto **Workspace** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

**DBEngine**. **Espaços de trabalho** (0)

**DBEngine**. **Espaços de trabalho** ("nome")

**DBEngine**. **Espaços de trabalho** \! \[nome\]

> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.


## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto Microsoft Access Workspace e o acrescenta à coleção **Workspaces**. Em seguida, enumeram-se as coleções **Workspaces** e a coleção **Properties** de cada objeto **Workspace**.

```vb 
Sub WorkspaceX() 
 
   Dim wrkNewAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
   ' Create a new Microsoft Access workspace. 
   Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
      "admin", "", dbUseJet) 
   Workspaces.Append wrkNewAcc 
 
   ' Enumerate the Workspaces collection. 
   For Each wrkLoop In Workspaces 
      With wrkLoop 
         Debug.Print "Properties of " & .Name 
         ' Enumerate the Properties collection of the new 
         ' Workspace object. 
         For Each prpLoop In .Properties 
            On Error Resume Next 
            If prpLoop <> "" Then Debug.Print "  " & _ 
               prpLoop.Name & " = " & prpLoop 
            On Error GoTo 0 
         Next prpLoop 
      End With 
   Next wrkLoop 
 
   wrkNewAcc.Close 
End Sub 
```

<br/>

Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho do Microsoft Access e um espaço de trabalho do ODBCDirect. Em seguida, listam-se as propriedades dos dois tipos de espaços de trabalho.

```vb 
Sub CreateWorkspaceX() 
 
   Dim wrkAcc As Workspace 
   Dim wrkLoop As Workspace 
   Dim prpLoop As Property 
 
 
   DefaultType = dbUseJet 
   ' Create an unnamed Workspace object of the type  
   ' specified by the DefaultType property of DBEngine  
   ' (dbUseJet). 
   Set wrkAcc = CreateWorkspace("", "admin", "") 
 
   ' Enumerate Workspaces collection. 
   Debug.Print "Workspace objects in Workspaces collection:" 
   For Each wrkLoop In Workspaces 
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
```

<br/>

O exemplo a seguir mostra como usar uma transação em um espaço de trabalho de Data Access Objects (DAO).

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Public Sub TransferFunds()
        Dim wrk As DAO.Workspace
        Dim dbC As DAO.Database
        Dim dbX As DAO.Database
        
        Set wrk = DBEngine(0)
        Set dbC = CurrentDb
        Set dbX = wrk.OpenDatabase("e:\books\acc2007vba\myDB.accdb")
        
        On Error GoTo trans_Err
        
        'Begin the transaction
        
        wrk.BeginTrans
        
        'Withdraw funds from one account table
        dbC.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT -20, 'DEBIT', Date()", dbFailOnError
    
        'Deposit funds into another account table
        dbX.Execute "INSERT INTO tblAccounts ( Amount, Txn, TxnDate ) SELECT 20, 'CREDIT', Date()", dbFailOnError
        
        'Commit the transaction
        wrk.CommitTrans dbForceOSFlush
        
    trans_Exit:
        'Clean up
        wrk.Close
        Set dbC = Nothing
        Set dbX = Nothing
        Set wrk = Nothing
        Exit Sub
        
    trans_Err:
        'Roll back the transaction
        wrk.Rollback
        Resume trans_Exit
        
    End Sub
```
