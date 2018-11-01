---
title: Método Cancel (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868740"
---
# <a name="cancel-method-rds"></a>Método Cancel (RDS)


**Aplica-se a**: Access 2013, o Office 2013

Cancela a execução de uma chamada de método assíncrona pendente.

## <a name="syntax"></a>Sintaxe

O *RDS*. *DataControl*. Cancelar

## <a name="remarks"></a>Comentários

Ao chamar **Cancel**, [ReadyState](readystate-property-rds.md) é automaticamente definido como **adcReadyStateLoaded** e o [Recordset](recordset-object-ado.md) estará vazio.

