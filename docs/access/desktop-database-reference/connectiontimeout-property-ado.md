---
title: Propriedade ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0526ee6a0d6cf9aa8f9263e8f3d31e66fad7da82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295699"
---
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="aec98-102">Propriedade ConnectionTimeout (ADO)</span><span class="sxs-lookup"><span data-stu-id="aec98-102">ConnectionTimeout property (ADO)</span></span>


<span data-ttu-id="aec98-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aec98-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aec98-104">Indica quanto tempo esperar ao estabelecer uma conexão antes de abortar a tentativa e gerar um erro.</span><span class="sxs-lookup"><span data-stu-id="aec98-104">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="aec98-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aec98-105">Settings and return values</span></span>

<span data-ttu-id="aec98-106">Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que a conexão seja aberta.</span><span class="sxs-lookup"><span data-stu-id="aec98-106">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open.</span></span> <span data-ttu-id="aec98-107">O padrão é 15.</span><span class="sxs-lookup"><span data-stu-id="aec98-107">Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec98-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec98-108">Remarks</span></span>

<span data-ttu-id="aec98-p102">Use a propriedade **ConnectionTimeout** em um objeto [Connection](connection-object-ado.md) se os atrasos no tráfego da rede ou o uso intenso do servidor tornarem necessário o abandono da tentativa de conexão. Se o tempo de definição da propriedade **ConnectionTimeout** terminar antes da abertura da conexão, um erro será gerado e o ADO cancelará a tentativa. Se você definir a propriedade como zero, o ADO esperará indefinidamente até que conexão seja aberta. Verifique se o provedor no qual você está escrevendo o código oferece suporte à funcionalidade **ConnectionTimeout**.</span><span class="sxs-lookup"><span data-stu-id="aec98-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="aec98-113">A propriedade **ConnectionTimeout** será leitura/gravação quando a conexão estiver fechada e somente leitura quando ela estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="aec98-113">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

