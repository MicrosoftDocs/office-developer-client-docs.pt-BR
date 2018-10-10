---
title: Propriedade Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f35dad5b7a8aa8dea543d689406b20e23221343a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464609"
---
# <a name="recordset2lockedits-property-dao"></a>Propriedade Recordset2.LockEdits (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que indica o tipo de bloqueio ativo durante a edição.

## <a name="syntax"></a>Sintaxe

*expressão* . LockEdits

*expressão* Uma variável que representa um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

O valor de configuração ou de retorno indica o tipo de bloqueio, conforme especificado na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>True</p></td>
<td><p>Padrão. Bloqueio pessimista ativo. A página que contém o registro que você estiver editando será bloqueada assim que for chamado o método Edit.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>Bloqueio otimista está em vigor para edição. A página que contém o registro não está protegida até que o método de atualização é executado.</p></td>
</tr>
</tbody>
</table>


Use a propriedade **LockEdits** com os objetos **[Recordset](recordset-object-dao.md)** atualizáveis.

Se uma página estiver bloqueada, nenhum outro usuário poderá editar registros na mesma página. Se você definir **LockEdits** como **True** e outro usuário já tiver bloqueado a página, ocorrerá um erro quando você usar o método **Edit**. Os outros usuários poderão ler os dados das páginas bloqueadas.

Se você definir a propriedade **LockEdits** como **False** e mais tarde usar o método **Update** ao mesmo tempo que outro usuário bloquear a página, ocorrerá um erro. Para ver as alterações feitas no seu registro pelo outro usuário, use o método **[Move](recordset2-move-method-dao.md)** com 0 como argumento; no entanto, se você fizer isso, perderá todas as suas alterações.

Durante o trabalho com o mecanismo do banco de dados do Microsoft Access conectado a fontes de dados ODBC, a propriedade **LockEdits** será definida sempre como **False** ou bloqueio otimista. O mecanismo de dados do Microsoft Access não tem controle sobre os mecanismos de bloqueio usados nos servidores de bancos de dados externos.


> [!NOTE]
> <P>Você pode predefinir o valor da <STRONG>LockEdits</STRONG> quando você primeiro abre o <STRONG>Recordset</STRONG> , definindo o argumento lockedits do método <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> . Definir o argumento lockedits como <STRONG>dbPessimistic</STRONG> definirá a propriedade <STRONG>LockEdits</STRONG> como <STRONG>True</STRONG>e lockedits de configuração para qualquer outro valor definirá a propriedade <STRONG>LockEdits</STRONG> como <STRONG>False</STRONG>.</P>



## <a name="example"></a>Exemplo

Este exemplo demonstra o bloqueio pessimista pela definição da propriedade **LockEdits** como **True** e depois demonstra o bloqueio otimista pela definição da propriedade **LockEdits** como False. Além disso, demonstra qual tipo de tratamento de erros será necessário em um ambiente de banco de dados multiusuário para modificar um campo. As funções PessimisticLock e OptimisticLock são necessárias para executar esse procedimento.

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
