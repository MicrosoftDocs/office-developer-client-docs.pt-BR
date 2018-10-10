---
title: Seção logs do arquivo de personalização
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464747"
---
# <a name="customization-file-logs-section"></a>Seção logs do arquivo de personalização

**Aplica-se a**: Access 2013 | Office 2013

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

