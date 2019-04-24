---
title: Método DBEngine. createWorkspace (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 9cd84b6b5441edda2042ce0a63ae25b2cf399bd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294342"
---
# <a name="dbenginecreateworkspace-method-dao"></a>Método DBEngine. createWorkspace (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto **[Workspace](workspace-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . CreateWorkspace (***nome***, ***nome de usuário***, ***senha***, ***UseType***)

*expressão* Uma variável que representa um objeto **DBEngine** .

## <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Nome</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes de <strong>espaço de trabalho</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>UserName</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Um <strong>String</strong> que identifica o proprietário do novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong>UserName</strong> para obter mais informações.</p></td>
</tr>
<tr class="odd">
<td><p><em>Password</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma <strong>cadeia de caracteres</strong> que contém a senha do novo objeto <strong>Workspace</strong> . A senha pode ter até 20 caracteres e incluir quaisquer caracteres exceto o caractere ASCII 0 (nulo).</p>
<p><strong>Observação</strong>: Use senhas fortes que combinam letras maiúsculas e minúsculas, números e símbolos. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</p>
</td>
</tr>
<tr class="even">
<td><p><em>UseType</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</p>
<p><strong>Observação</strong>: os espaços de trabalho ODBCDirect não têm suporte no Microsoft Access 2013. Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Espaço de trabalho

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

