---
title: Seção Connect do arquivo de personalização
TOCTitle: Customization File Connect section
ms:assetid: 037abfb4-798d-4b09-6133-356969aee95c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248802(v=office.15)
ms:contentKeyID: 48542985
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49e2d6cc8579f064df3e752268fce5b47c9b1ada
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944183"
---
# <a name="customization-file-connect-section"></a>Seção Connect do arquivo de personalização

**Aplica-se a**: Access 2013, o Office 2013

O comportamento padrão do manipulador é negar todas as conexões. A seção **connect** especifica exceções a esse comportamento. Por exemplo, se todas as seções **connect** estivessem ausentes ou vazias, nenhuma conexão seria estabelecida por padrão.

A seção **connect** pode conter:

- Uma entrada de acesso padrão que especifica as operações de leitura e gravação padrão permitidas na conexão. Se a seção não tiver entrada de acesso padrão, ela será ignorada.

- Uma nova sequência de conexão que substitui a sequência de conexão do cliente.

## <a name="syntax"></a>Sintaxe

Uma entrada de acesso padrão tem este formato:

`Access=accessRight`

Uma entrada de sequência de substituição de conexão tem este formato:

`Connect=connectionString`

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
<td><p><strong>Connect</strong></p></td>
<td><p>Uma sequência literal que indica uma entrada de sequência de conexão.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>connectionString</em></strong></p></td>
<td><p>Uma sequência de caracteres que substitui toda a sequência de conexão do cliente.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Access</strong></p></td>
<td><p>Uma sequência literal que indica uma entrada de acesso.</p></td>
</tr>
<tr class="even">
<td><p><strong><em>accessRight</em></strong></p></td>
<td><p>Um dos seguintes direitos de acesso:
</p>
<p></p>
<ul>
<li><p><strong>NoAccess</strong> — o usuário não pode acessar a fonte de dados.</p></li>
<li><p><strong>ReadOnly</strong> — o usuário pode ler a fonte de dados.</p></li>
<li><p><strong>ReadWrite</strong> — o usuário pode ler a fonte de dados ou gravar nela.</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>


Se você quiser permitir que qualquer conexão (desabilitando o comportamento padrão do manipulador), defina a entrada de acesso na seção **Conectar padrão** e exclua ou comente qualquer outra **Conectar** *identificador de* seção.

