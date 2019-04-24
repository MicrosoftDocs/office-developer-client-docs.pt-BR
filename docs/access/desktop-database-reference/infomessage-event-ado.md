---
title: Evento InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291439"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="32d20-102">Evento InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="32d20-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="32d20-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32d20-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32d20-104">O evento **InfoMessage** é chamado sempre que ocorre um aviso durante uma operação **ConnectionEvent**.</span><span class="sxs-lookup"><span data-stu-id="32d20-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32d20-105">Syntax</span></span>

<span data-ttu-id="32d20-106">InfoMessage*perror*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="32d20-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="32d20-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32d20-107">Parameters</span></span>

|<span data-ttu-id="32d20-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="32d20-108">Parameter</span></span>|<span data-ttu-id="32d20-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="32d20-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="32d20-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="32d20-110">*pError*</span></span> |<span data-ttu-id="32d20-p101">Um objeto [Error](error-object-ado.md). Este parâmetro contém quaisquer erros que são retornados. Se vários erros forem retornados, enumere a coleção de **Erros** para localizá-los.</span><span class="sxs-lookup"><span data-stu-id="32d20-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="32d20-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="32d20-114">*adStatus*</span></span> |<span data-ttu-id="32d20-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="32d20-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="32d20-116">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="32d20-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="32d20-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="32d20-117">*pConnection*</span></span> |<span data-ttu-id="32d20-p103">Um objeto [Connection](connection-object-ado.md). A conexão para a qual o aviso ocorreu. Por exemplo, os avisos podem ocorrer ao abrir um objeto **Connection** ou ao executar um [Comando](command-object-ado.md) em uma **Conexão**.</span><span class="sxs-lookup"><span data-stu-id="32d20-p103">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

