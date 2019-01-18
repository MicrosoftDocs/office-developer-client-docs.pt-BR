---
title: Método QueryDef.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720551"
---
# <a name="querydefcancel-method-dao"></a>Método QueryDef.Cancel (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Cancelar

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync). **Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.

