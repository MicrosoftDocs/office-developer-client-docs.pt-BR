---
title: Método DBEngine.RegisterDatabase (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 304f517d11e6e333bb0455e3882421c410c56b72
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462946"
---
# <a name="dbengineregisterdatabase-method-dao"></a>Método DBEngine.RegisterDatabase (DAO)


**Aplica-se a**: Access 2013 | Office 2013


Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.

## <a name="syntax"></a>Sintaxe

*expressão* . RegisterDatabase (***Dsn***, ***Driver***, ***silenciosa***, ***atributos***)

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
<td><p>DSN</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome usado no método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>. Ele se refere a um bloco de informações descritivas sobre a fonte de dados. Por exemplo, se a fonte de dados for um banco de dados remoto ODBC, ele poderá ser o nome do servidor.</p></td>
</tr>
<tr class="even">
<td><p>Driver</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome do driver ODBC. Esse não é o nome do arquivo DLL do driver ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Silenciosa</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>True</strong> se você não quiser exibir as caixas de diálogo de driver ODBC que solicita informações específicas do driver; ou <strong>False</strong> se você deseja exibir as caixas de diálogo do driver ODBC. Se silenciosa for <strong>True</strong>, atributos devem conter todas as informações necessárias específicas do driver ou as caixas de diálogo serão exibidas mesmo assim.</p></td>
</tr>
<tr class="even">
<td><p>Atributos</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Uma lista de palavras-chave a serem adicionadas ao Registro do Windows. As palavras-chave estão em uma sequência delimitada por retorno de carro.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se o banco de dados já estiver registrado (as informações de conexão já estarão inseridas) no Registro do Windows quando você usar o método **RegisterDatabase**, as informações de conexão serão atualizadas.

Se o método **RegisterDatabase** falhar por qualquer motivo, nenhuma alteração será feita no Registro do Windows, e ocorrerá um erro.

Para obter mais informações sobre drivers ODBC, como SQL Server, consulte o arquivo de Ajuda fornecido com o driver.

## <a name="example"></a>Exemplo

Este exemplo utiliza o método **RegisterDatabase** para registrar uma fonte de dados do Microsoft SQL Server chamada Publishers no Registro do Windows.

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

