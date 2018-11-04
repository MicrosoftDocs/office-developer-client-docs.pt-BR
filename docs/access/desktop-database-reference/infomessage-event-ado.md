---
title: Evento InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1db793ec99dd0248eacc527bd76068ceec025a58
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949429"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="ea08c-102">Evento InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea08c-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="ea08c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea08c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ea08c-104">O evento **InfoMessage** é chamado sempre que ocorre um aviso durante uma operação **ConnectionEvent**.</span><span class="sxs-lookup"><span data-stu-id="ea08c-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea08c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea08c-105">Syntax</span></span>

<span data-ttu-id="ea08c-106">InfoMessage*pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="ea08c-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="ea08c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea08c-107">Parameters</span></span>

|<span data-ttu-id="ea08c-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea08c-108">Parameter</span></span>|<span data-ttu-id="ea08c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea08c-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ea08c-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="ea08c-110">*pError*</span></span> |<span data-ttu-id="ea08c-p101">Um objeto [Error](error-object-ado.md). Este parâmetro contém quaisquer erros que são retornados. Se vários erros forem retornados, enumere a coleção de **Erros** para localizá-los.</span><span class="sxs-lookup"><span data-stu-id="ea08c-p101">An [Error](error-object-ado.md) object. This parameter contains any errors that are returned. If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="ea08c-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="ea08c-114">*adStatus*</span></span> |<span data-ttu-id="ea08c-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="ea08c-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="ea08c-116">Antes de este evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ea08c-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="ea08c-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="ea08c-117">*pConnection*</span></span> |<span data-ttu-id="ea08c-p103">Um objeto [Connection](connection-object-ado.md). A conexão para a qual o aviso ocorreu. Por exemplo, os avisos podem ocorrer ao abrir um objeto **Connection** ou ao executar um [Comando](command-object-ado.md) em uma **Conexão**.</span><span class="sxs-lookup"><span data-stu-id="ea08c-p103">A [Connection](connection-object-ado.md) object. The connection for which the warning occurred. For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

