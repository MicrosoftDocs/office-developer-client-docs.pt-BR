---
title: Microsoft OLE DB Provider for Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288929"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Provedor Microsoft OLE DB para Oracle

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft OLE DB Provider for Oracle permite que o ADO acesse bancos de dados Oracle.

## <a name="connection-string-parameters"></a>Parâmetros da sequência de conexão

Para conectar-se a esse provedor, defina o argumento *Provider* da propriedade [ConnectionString](connectionstring-property-ado.md) como:

```vb 
 
MSDAORA 
```

A leitura da propriedade [Provider](provider-property-ado.md) também retornará essa cadeia de caracteres.

Se uma consulta de junção com um cursor de conjunto de chaves ou dinâmico for executada em um banco de dados Oracle, ocorrerá um erro. O Oracle oferece suporte apenas a cursores estáticos somente leitura.

## <a name="typical-connection-string"></a>Sequência de conexão típica

Esta é uma sequência de conexão típica para esse provedor:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

A cadeia de caracteres consiste nas seguintes palavras-chave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palavra-chave</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica o Microsoft OLE DB Provider for Oracle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica o nome de um servidor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica o nome do usuário.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica a senha do usuário.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Parâmetros de conexão específicos para provedor

O provedor oferece suporte a vários parâmetros de conexão específicos para provedor, além daqueles definidos pelo ADO. Assim como as propriedades de conexão do ADO, essas propriedades específicas para provedor também podem ser definidas por meio da coleção [Properties](properties-collection-ado.md) de um objeto [Connection](connection-object-ado.md) ou como parte da **ConnectionString**.

Esses parâmetros são descritos integralmente na Referência do programador do OLE DB. (O [Índice da propriedade dinâmica do ADO](ado-dynamic-property-index.md) fornece uma referência cruzada entre esses nomes de parâmetros e as propriedades do OLE DB correspondentes.)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parâmetro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Window Handle</strong></p></td>
<td><p>Indica o identificador da janela que deverá ser usado para solicitar informações adicionais.</p></td>
</tr>
<tr class="even">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Indica um número único de 32 bits (por exemplo, 1033) que especifica preferências relacionadas ao idioma do usuário. Essas preferências indicam como as datas e os horários serão formatados, se os itens serão classificados em ordem alfabética, como as cadeias de caracteres serão comparadas, e assim por diante.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OLE DB Services</strong></p></td>
<td><p>Indica uma máscara de bits especificando os serviços do OLE DB que deverão ser habilitados ou desabilitados.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Indica se o usuário deverá ser avisado enquanto uma conexão estiver sendo estabelecida.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Extended Properties</strong></p></td>
<td><p>Uma cadeia de caracteres contendo informações de conexão estendidas específicas para provedor. Use esta propriedade somente para informações de conexão específicas para provedor que não possam ser descritas pelo mecanismo de propriedades.</p></td>
</tr>
</tbody>
</table>

