---
title: Enumeração driverPromptEnum (DAO)
TOCTitle: DriverPromptEnum Enumeration
ms:assetid: 8dda5e9f-a58f-a62d-eb49-5966d4a1e086
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197361(v=office.15)
ms:contentKeyID: 48546266
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9612c0713a86ed6ad34a5eff61e45efcddf6cf24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293662"
---
# <a name="driverpromptenum-enumeration-dao"></a><span data-ttu-id="f3a62-102">Enumeração driverPromptEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3a62-102">DriverPromptEnum enumeration (DAO)</span></span>


<span data-ttu-id="f3a62-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3a62-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3a62-104">Especifica se e quando o usuário deve ser solicitado a estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="f3a62-104">Specifies if and when to prompt the user to establish a connection.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3a62-105">Nome</span><span class="sxs-lookup"><span data-stu-id="f3a62-105">Name</span></span></p></th>
<th><p><span data-ttu-id="f3a62-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f3a62-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f3a62-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3a62-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3a62-108">dbDriverComplete</span><span class="sxs-lookup"><span data-stu-id="f3a62-108">dbDriverComplete</span></span></p></td>
<td><p><span data-ttu-id="f3a62-109">0</span><span class="sxs-lookup"><span data-stu-id="f3a62-109">0</span></span></p></td>
<td><p><span data-ttu-id="f3a62-110">Se a sequência de conexão fornecida incluir a palavra-chave DSN, o gerenciador de driver utilizará a sequência de caracteres, conforme fornecida na conexão. Caso contrário, seu comportamento será o mesmo de quando <strong>dbDriverPrompt</strong> é especificado.</span><span class="sxs-lookup"><span data-stu-id="f3a62-110">If the connection string provided includes the DSN keyword, the driver manager uses the string as provided in connect, otherwise it behaves as it does when <strong>dbDriverPrompt</strong> is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3a62-111">dbDriverCompleteRequired</span><span class="sxs-lookup"><span data-stu-id="f3a62-111">dbDriverCompleteRequired</span></span></p></td>
<td><p><span data-ttu-id="f3a62-112">3 </span><span class="sxs-lookup"><span data-stu-id="f3a62-112">3</span></span></p></td>
<td><p><span data-ttu-id="f3a62-113">(Padrão) Comporta-se como <strong>dbDriverComplete</strong>, exceto pelo fato de que o driver desabilita os controles de quaisquer informações que não sejam necessárias para concluir a conexão.</span><span class="sxs-lookup"><span data-stu-id="f3a62-113">(Default) Behaves like <strong>dbDriverComplete</strong> except the driver disables the controls for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f3a62-114">dbDriverNoPrompt</span><span class="sxs-lookup"><span data-stu-id="f3a62-114">dbDriverNoPrompt</span></span></p></td>
<td><p><span data-ttu-id="f3a62-115">1 </span><span class="sxs-lookup"><span data-stu-id="f3a62-115">1</span></span></p></td>
<td><p><span data-ttu-id="f3a62-p101">O gerenciador de driver usa a sequência de conexão fornecida na conexão. Se não forem fornecidas informações suficientes, será retornado um erro interceptável.</span><span class="sxs-lookup"><span data-stu-id="f3a62-p101">The driver manager uses the connection string provided in connect. If sufficient information is not provided, a trappable error is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f3a62-118">dbDriverPrompt</span><span class="sxs-lookup"><span data-stu-id="f3a62-118">dbDriverPrompt</span></span></p></td>
<td><p><span data-ttu-id="f3a62-119">2 </span><span class="sxs-lookup"><span data-stu-id="f3a62-119">2</span></span></p></td>
<td><p><span data-ttu-id="f3a62-p102">O gerenciador de driver exibe a caixa de diálogo <strong>Fontes de Dados ODBC</strong>. A sequência de conexão usada para estabelecer a conexão é construída a partir do DSN (nome da fonte de dados) selecionado e é completada pelo usuário por meio das caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f3a62-p102">The driver manager displays the <strong>ODBC Data Sources</strong> dialog box. The connection string used to establish the connection is constructed from the data source name (DSN) selected and completed by the user via the dialog boxes.</span></span></p></td>
</tr>
</tbody>
</table>

