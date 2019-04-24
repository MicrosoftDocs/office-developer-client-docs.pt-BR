---
title: Noções básicas sobre o arquivo de personalização
TOCTitle: Understanding the Customization File
ms:assetid: 98fd5ec1-d5bd-cdd2-5eb5-9a1682fbed79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249686(v=office.15)
ms:contentKeyID: 48546507
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b977fc4273068ac52efe8960761a9e28a6234e2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314067"
---
# <a name="understanding-the-customization-file"></a>Noções básicas sobre o arquivo de personalização


**Aplica-se ao:** Access 2013, Office 2013

Cada cabeçalho de seção no arquivo de personalização consiste em colchetes (**\[**) contendo um tipo e parâmetro. Os quatro tipos de seção são indicados pela sequência de caracteres literal **connect**, **sql**, **userlist** ou **logs**. O parâmetro pode ser a sequência de caracteres literal, o padrão, um identificador especificado pelo usuário ou nada.

Portanto, cada seção é marcada com um destes cabeçalhos de seção:

```text 
 
[ connect   default     ]
[ connect   identifier  ]
[ sql       default     ]
[ sql       identifier  ]
[ userlist  identifier  ]
[ logs                  ]
```

Os cabeçalhos de seção possuem as seguintes partes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parte</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>ao</strong></p></td>
<td><p>Uma sequência de caracteres literal que modifica uma sequência de conexão.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Uma sequência de caracteres literal que modifica uma sequência de comando.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UserList</strong></p></td>
<td><p>Uma sequência de caracteres literal que modifica os direitos de acesso de um usuário específico.</p></td>
</tr>
<tr class="even">
<td><p><strong>logs</strong></p></td>
<td><p>Uma sequência de caracteres literal que especifica um arquivo de log que registra erros operacionais.</p></td>
</tr>
<tr class="odd">
<td><p><strong>default</strong></p></td>
<td><p>Uma sequência de caracteres literal usada quando nenhum identificador é especificado ou localizado.</p></td>
</tr>
<tr class="even">
<td><p><em>identificador</em></p></td>
<td><p>Uma sequência de caracteres que corresponde a uma sequência de caracteres na sequência de <strong>conexão</strong> ou de <strong>comando</strong>.</p>
<p></p>
<ul>
<li><p>Use esta seção se o cabeçalho de seção contiver <strong>connect</strong> e a sequência identifier for localizada na sequência de conexão.</p></li>
<li><p>Use esta seção se o cabeçalho de seção contiver <strong>sql</strong> e a sequência identifier for localizada na sequência de comando.</p></li>
<li><p>Use esta seção se o cabeçalho de seção contiver <strong>userlist</strong> e a sequência identifier corresponder a um identificador de seção <strong>connect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


O **DataFactory** chama o manipulador, passando parâmetros cliente. O manipulador procura sequências de caracteres completas nesses parâmetros que correspondam aos identificadores nos cabeçalhos de seção apropriados. Se for encontrada uma correspondência, o conteúdo dessa seção será aplicado ao parâmetro cliente.

Uma seção específica é usada nas seguintes circunstâncias:

  - Uma seção **Connect** será usada se a parte de valor da palavra-chave cadeia de caracteres de conexão do cliente, "**fonte de dados = * * * valor*", corresponder a um identificador de seção **Connect** *.*

  - Uma seção **sql** será usada se a sequência de comando do cliente contiver uma sequência de caracteres que corresponda a um identificador de seção **sql**.

  - Uma seção **connect** ou **sql** com um parâmetro padrão será usada se não houver nenhum identificador correspondente.

  - Uma seção **userlist** será usada se o identificador da seção **userlist** corresponder a um identificador da seção **connect**. Em caso de correspondência, o conteúdo da seção **userlist** será aplicado à conexão administrada pela seção **connect**.

  - Se a sequência de caracteres em uma sequência de conexão ou de comando não corresponder ao identificador de nenhum cabeçalho da seção **connect** ou **sql** e se não houver cabeçalho da seção **connect** ou **sql** com um parâmetro padrão, a sequência de caracteres do cliente será usada sem modificação.

  - A seção **logs** será usada sempre que **DataFactory** estiver em operação.

