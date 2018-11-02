---
title: Evento onReadyStateChange (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3e52ef236a5e57efc965a6b3bd8ab6edd7533f2c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922206"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="7b978-102">Evento onReadyStateChange (RDS)</span><span class="sxs-lookup"><span data-stu-id="7b978-102">onReadyStateChange event (RDS)</span></span>


<span data-ttu-id="7b978-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b978-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="7b978-104">O evento **onReadyStateChange** é chamado sempre que o valor da propriedade [ReadyState](readystate-property-rds.md) é alterado.</span><span class="sxs-lookup"><span data-stu-id="7b978-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b978-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b978-105">Syntax</span></span>

<span data-ttu-id="7b978-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="7b978-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="7b978-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b978-107">Parameters</span></span>

<span data-ttu-id="7b978-108">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7b978-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b978-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b978-109">Remarks</span></span>

<span data-ttu-id="7b978-p101">A propriedade **ReadyState** reflete o andamento de um objeto [RDS.DataControl](datacontrol-object-rds.md) uma vez que ele recupera, de maneira assíncrona, os dados em seu objeto [Recordset](recordset-object-ado.md). Use o evento **onReadyStateChange** para monitorar as alterações na propriedade **ReadyState** sempre que elas ocorrerem. Isso é mais eficiente do que verificar periodicamente o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7b978-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

