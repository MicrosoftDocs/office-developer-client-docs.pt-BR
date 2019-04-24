---
title: Método Cancel (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296644"
---
# <a name="cancel-method-rds"></a>Método Cancel (RDS)


**Aplica-se ao:** Access 2013, Office 2013

Cancela a execução de uma chamada de método assíncrona pendente.

## <a name="syntax"></a>Sintaxe

*RDS*. *DataControl*. Cancelar

## <a name="remarks"></a>Comentários

Ao chamar **Cancel**, [ReadyState](readystate-property-rds.md) é automaticamente definido como **adcReadyStateLoaded** e o [Recordset](recordset-object-ado.md) estará vazio.

