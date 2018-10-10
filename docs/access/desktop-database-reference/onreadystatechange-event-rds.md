---
title: Evento onReadyStateChange (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dec783aaa76745b73bd031b00f1b8587a58eb165
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464148"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="f71b4-102">Evento onReadyStateChange (RDS)</span><span class="sxs-lookup"><span data-stu-id="f71b4-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="f71b4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f71b4-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f71b4-104">O evento **onReadyStateChange** é chamado sempre que o valor da propriedade [ReadyState](readystate-property-rds.md) é alterado.</span><span class="sxs-lookup"><span data-stu-id="f71b4-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71b4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f71b4-105">Syntax</span></span>

<span data-ttu-id="f71b4-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="f71b4-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="f71b4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f71b4-107">Parameters</span></span>

<span data-ttu-id="f71b4-108">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f71b4-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f71b4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f71b4-109">Remarks</span></span>

<span data-ttu-id="f71b4-p101">A propriedade **ReadyState** reflete o andamento de um objeto [RDS.DataControl](datacontrol-object-rds.md) uma vez que ele recupera, de maneira assíncrona, os dados em seu objeto [Recordset](recordset-object-ado.md). Use o evento **onReadyStateChange** para monitorar as alterações na propriedade **ReadyState** sempre que elas ocorrerem. Isso é mais eficiente do que verificar periodicamente o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f71b4-p101">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object. Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur. This is more efficient than periodically checking the property's value.</span></span>

