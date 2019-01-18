---
title: Seção Logs do arquivo de personalização
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715631"
---
# <a name="customization-file-logs-section"></a>Seção Logs do arquivo de personalização

**Aplica-se a**: Access 2013, o Office 2013

A seção **logs** contém uma entrada de arquivo de log que especifica o nome de um arquivo responsável pelo registro de erros durante a operação do **DataFactory**.

## <a name="syntax"></a>Sintaxe

Uma entrada de arquivo de log tem este formato:

`err=FileName`

<br/>

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
<td><p><strong>err</strong></p></td>
<td><p>Uma sequência literal que indica uma entrada de arquivo de log.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Um nome de arquivo e um caminho completo. O nome típico de arquivo é <strong>c:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


O arquivo de log conterá o nome de usuário, HRESULT, a data e a hora de cada erro.

