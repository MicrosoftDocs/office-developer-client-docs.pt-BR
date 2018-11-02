---
title: Propriedade InternetTimeout (RDS)
TOCTitle: InternetTimeout property (RDS)
ms:assetid: 66fc6e87-3d23-ce2c-18f5-0fc83ac43801
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249401(v=office.15)
ms:contentKeyID: 48545353
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1287289de5ef303e41a342ef84822d3a14083470
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918804"
---
# <a name="internettimeout-property-rds"></a><span data-ttu-id="31d84-102">Propriedade InternetTimeout (RDS)</span><span class="sxs-lookup"><span data-stu-id="31d84-102">InternetTimeout property (RDS)</span></span>


<span data-ttu-id="31d84-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="31d84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31d84-104">Indica o tempo de espera, em milissegundos, antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="31d84-104">Indicates the number of milliseconds to wait before a request times out.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="31d84-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="31d84-105">Settings and return values</span></span>

<span data-ttu-id="31d84-106">Define ou retorna um valor **Long** que representa o número de milissegundos antes do tempo limite de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="31d84-106">Sets or returns a **Long** value that represents the number of milliseconds before a request will time out.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d84-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="31d84-107">Remarks</span></span>

<span data-ttu-id="31d84-108">Esta propriedade aplica-se apenas às solicitações enviadas com os protocolos HTTP ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="31d84-108">This property applies only to requests sent with the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="31d84-p101">Solicitações em um ambiente de três camadas podem demorar alguns minutos para serem executadas. Use esta propriedade para especificar o tempo adicional para solicitações longas.</span><span class="sxs-lookup"><span data-stu-id="31d84-p101">Requests in a three-tier environment can take several minutes to execute. Use this property to specify additional time for long-running requests.</span></span>

