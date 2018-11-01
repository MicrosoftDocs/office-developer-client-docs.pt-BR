---
title: Características do cursor e do bloqueio
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85268b9c4b57d92cd8e7df9cd1da01286709f915
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877566"
---
# <a name="cursor-and-lock-characteristics"></a>Características do cursor e do bloqueio


**Aplica-se a**: Access 2013, o Office 2013

Embora as características de um cursor dependam dos recursos do provedor, as vantagens e desvantagens a seguir em geral se aplicam aos vários tipos de cursores e bloqueios.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Tipo de cursor ou bloqueio</p></th>
<th><p>Vantagens</p></th>
<th><p>Desvantagens</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Baixa necessidade de recursos</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Não é possível rolar para trás</p></li>
<li><p>Não há simultaneidade de dados</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Rolável</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Não há simultaneidade de dados</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Alguma simultaneidade de dados</p></li>
<li><p>Rolável</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Maior necessidade de recursos</p></li>
<li><p>Não disponível em cenário desconectado</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Alta simultaneidade de dados</p></li>
<li><p>Rolável</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Alta necessidade de recursos</p></li>
<li><p>Não disponível em cenário desconectado</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Baixa necessidade de recursos</p></li>
<li><p>Altamente escalonável</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Dados não atualizáveis através do cursor</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Atualizações em lotes</p></li>
<li><p>Permite cenários desconectados</p></li>
<li><p>Outros usuários podem acessar os dados</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Os dados podem ser alterados por vários usuários ao mesmo tempo</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Os dados não podem ser alterados por outros usuários durante o bloqueio</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Impede que outros usuários acessem os dados durante o bloqueio</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Outros usuários podem acessar os dados</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Os dados podem ser alterados por vários usuários ao mesmo tempo</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

