---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929b166a308276836fbe4a48a2461ef7eb0caba2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461981"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="77719-102">Propriedade InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="77719-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="77719-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="77719-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="77719-104">Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="77719-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="77719-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="77719-105">Settings and Return Values</span></span>

<span data-ttu-id="77719-106">Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="77719-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="77719-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="77719-107">Remarks</span></span>

<span data-ttu-id="77719-108">Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="77719-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="77719-p101">Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.</span><span class="sxs-lookup"><span data-stu-id="77719-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

