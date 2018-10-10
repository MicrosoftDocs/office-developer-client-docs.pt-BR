---
title: Método Cancel (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcd37f8736b7ab4b953480cd28daeb3080abe07f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462773"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="8642e-102">Método Cancel (RDS)</span><span class="sxs-lookup"><span data-stu-id="8642e-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="8642e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8642e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8642e-104">Cancela a execução de uma chamada de método assíncrona pendente.</span><span class="sxs-lookup"><span data-stu-id="8642e-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="8642e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8642e-105">Syntax</span></span>

<span data-ttu-id="8642e-106">O *RDS*.</span><span class="sxs-lookup"><span data-stu-id="8642e-106">*RDS*.</span></span> <span data-ttu-id="8642e-107">*DataControl*. Cancelar</span><span class="sxs-lookup"><span data-stu-id="8642e-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="8642e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="8642e-108">Remarks</span></span>

<span data-ttu-id="8642e-109">Ao chamar **Cancel**, [ReadyState](readystate-property-rds.md) é automaticamente definido como **adcReadyStateLoaded** e o [Recordset](recordset-object-ado.md) estará vazio.</span><span class="sxs-lookup"><span data-stu-id="8642e-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

