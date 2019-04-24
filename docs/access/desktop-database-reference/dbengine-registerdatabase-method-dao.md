---
title: Método DBEngine. RegisterDatabase (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294222"
---
# <a name="dbengineregisterdatabase-method-dao"></a>Método DBEngine. RegisterDatabase (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Insere as informações de conexão para uma fonte de dados ODBC no Registro do Windows. O driver ODBC precisa das informações de conexão quando a fonte de dados ODBC é aberta durante uma sessão.

## <a name="syntax"></a>Sintaxe

*expressão* . RegisterDatabase (***DSN***, ***Driver***, ***silencioso***, ***atributos***)

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
<td><p><em>DSN</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>o nome usado no método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> . Ele se refere a um bloco de informações descritivas sobre a fonte de dados. Por exemplo, se a fonte de dados for um banco de dados remoto ODBC, ele poderá ser o nome do servidor.</p></td>
</tr>
<tr class="even">
<td><p><em>Driver</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O nome do driver ODBC. Esse não é o nome do arquivo DLL do driver ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><em>Silenciosa</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Boolean</strong></p></td>
<td><p><strong>True</strong> se você não quiser exibir as caixas de diálogo do driver ODBC que solicitam as informações específicas do driver; ou <strong>False</strong> se você desejar exibir as caixas de diálogo do driver ODBC. Se silencioso for <strong>verdadeiro</strong>, os atributos deverão conter todas as informações específicas do driver necessárias ou as caixas de diálogo serão exibidas de qualquer forma.</p></td>
</tr>
<tr class="even">
<td><p><em>Atributos</em></p></td>
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

