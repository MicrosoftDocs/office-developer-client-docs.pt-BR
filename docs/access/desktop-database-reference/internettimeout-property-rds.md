---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout Property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06e844b9e6e0976679820fbc2ac79eae14131d36
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879037"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="0e870-102">Propriedade InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="0e870-102">InternetTimeout Property (RDS)</span></span>


<span data-ttu-id="0e870-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e870-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e870-104">Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="0e870-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0e870-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0e870-105">Settings and return values</span></span>

<span data-ttu-id="0e870-106">Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="0e870-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e870-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e870-107">Remarks</span></span>

<span data-ttu-id="0e870-108">Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0e870-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="0e870-p101">Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.</span><span class="sxs-lookup"><span data-stu-id="0e870-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

