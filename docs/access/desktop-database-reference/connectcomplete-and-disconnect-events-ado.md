---
title: Eventos ConnectComplete e Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295986"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="fa3e4-102">Eventos ConnectComplete e Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa3e4-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="fa3e4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa3e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa3e4-104">O evento **ConnectComplete** é chamado após o *início* de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="fa3e4-105">O evento **Disconnect** é chamado depois do *término* de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3e4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa3e4-106">Syntax</span></span>

<span data-ttu-id="fa3e4-107">ConnectComplete*perror*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="fa3e4-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="fa3e4-108">DesConectar*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="fa3e4-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="fa3e4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa3e4-109">Parameters</span></span>

|<span data-ttu-id="fa3e4-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa3e4-110">Parameter</span></span>|<span data-ttu-id="fa3e4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa3e4-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fa3e4-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="fa3e4-112">*pError*</span></span> |<span data-ttu-id="fa3e4-p102">Um objeto [Error](error-object-ado.md). Descreve o erro ocorrido se o valor de *adStatus* for **adStatusErrorsOccurred**; caso contrário, não será definido.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="fa3e4-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="fa3e4-115">*adStatus*</span></span> |<span data-ttu-id="fa3e4-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="fa3e4-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="fa3e4-117">Quando **ConnectComplete** é chamado, este parâmetro é definido como **adStatusCancel** se um evento **WillConnect** solicitou o cancelamento da conexão pendente.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="fa3e4-p104">Antes do evento retornar, defina este parâmetro como **adStatusUnwantedEvent** para evitar notificações subsequentes. Contudo, o fechamento e a reabertura de [Connection](connection-object-ado.md) faz com que esses eventos ocorram novamente.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-p104">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications. However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="fa3e4-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="fa3e4-120">*pConnection*</span></span> |<span data-ttu-id="fa3e4-121">O objeto **Connection** ao qual este evento se aplica.</span><span class="sxs-lookup"><span data-stu-id="fa3e4-121">The **Connection** object for which this event applies.</span></span>|

