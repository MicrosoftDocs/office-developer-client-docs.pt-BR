---
title: Método DBEngine.CreateWorkspace (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 039da9aeb6166b25b0800533f50aa7ec5053c3c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462005"
---
# <a name="dbenginecreateworkspace-method-dao"></a>Método DBEngine.CreateWorkspace (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Cria um novo objeto **[Workspace](workspace-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . CreateWorkspace (***nome***, ***nome de usuário***, ***senha***, ***UseType***)

*expressão* Uma variável que representa um objeto **DBEngine** .

### <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Workspace</strong>.</p></td>
</tr>
<tr class="even">
<td><p>UserName</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Um <strong>String</strong> que identifica o proprietário do novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong>UserName</strong> para obter mais informações.</p></td>
</tr>
<tr class="odd">
<td><p>Senha</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma <strong>cadeia de caracteres</strong> contendo a senha para o novo objeto <strong>Workspace</strong> . A senha pode ter até 20 caracteres e pode incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</p>

> [!NOTE]
> <P>[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</P>


</td>
</tr>
<tr class="even">
<td><p>UseType</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Definindo o argumento type como <STRONG>dbUseODBC</STRONG> resultará em um erro em tempo de execução. Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor retornado

Workspace

## <a name="remarks"></a>Comentários

Após usar o método **CreateWorkspace** para criar um novo objeto **Workspace**, uma sessão do **Workspace** será iniciada e você poderá fazer referência ao objeto **Workspace** em seu aplicativo.

Objetos **Workspace** não são permanentes e não podem ser salvos em disco. Após criar um objeto **Workspace**, você não poderá alterar suas configurações de propriedade, com exceção da propriedade **Name**, que você pode modificar antes de acrescentar o objeto **Workspace** à coleção **[Workspaces](workspaces-collection-dao.md)**.

Não é necessário acrescentar o novo objeto **Workspace** à coleção antes de usá-la. Acrescenta-se um objeto **Workspace** recém-criado apenas se for preciso fazer referência a ele por meio da coleção **Workspaces**.

Para remover um objeto **Workspace** da coleção **Workspaces**, feche todos os bancos de dados e conexões abertos e use o método **[Close](connection-close-method-dao.md)** no objeto **Workspace**.

## <a name="example"></a>Exemplo

Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho do Microsoft Access Em seguida, lista as propriedades do espaço de trabalho.

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

