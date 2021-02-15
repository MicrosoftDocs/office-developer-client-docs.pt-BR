---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0650a287e2aebc13b89572db112b8f9b333dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291238"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="6bcc6-102">Propriedade InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="6bcc6-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="6bcc6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6bcc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6bcc6-104">Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bcc6-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6bcc6-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6bcc6-105">Settings and return values</span></span>

<span data-ttu-id="6bcc6-106">Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6bcc6-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bcc6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bcc6-107">Remarks</span></span>

<span data-ttu-id="6bcc6-108">Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6bcc6-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="6bcc6-p101">Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.</span><span class="sxs-lookup"><span data-stu-id="6bcc6-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

