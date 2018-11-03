---
title: Seção de Logs do arquivo de personalização
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c9a8b9c2255825b135fbc181900a73b3686c64c7
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946143"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="5188c-102">Seção de Logs do arquivo de personalização</span><span class="sxs-lookup"><span data-stu-id="5188c-102">Customization File Logs section</span></span>

<span data-ttu-id="5188c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5188c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5188c-104">A seção **logs** contém uma entrada de arquivo de log que especifica o nome de um arquivo responsável pelo registro de erros durante a operação do **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="5188c-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5188c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5188c-105">Syntax</span></span>

<span data-ttu-id="5188c-106">Uma entrada de arquivo de log tem este formato:</span><span class="sxs-lookup"><span data-stu-id="5188c-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5188c-107">Parte</span><span class="sxs-lookup"><span data-stu-id="5188c-107">Part</span></span></p></th>
<th><p><span data-ttu-id="5188c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5188c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5188c-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="5188c-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="5188c-110">Uma sequência literal que indica uma entrada de arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="5188c-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5188c-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="5188c-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="5188c-p101">Um nome de arquivo e um caminho completo. O nome típico de arquivo é <strong>c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="5188c-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5188c-114">O arquivo de log conterá o nome de usuário, HRESULT, a data e a hora de cada erro.</span><span class="sxs-lookup"><span data-stu-id="5188c-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

