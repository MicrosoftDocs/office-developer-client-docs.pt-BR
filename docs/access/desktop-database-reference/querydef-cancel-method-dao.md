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
ms.openlocfilehash: 8e121457f7084b4d13e89c43a30a7632a3cd7377
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873975"
---
# <a name="querydefcancel-method-dao"></a>Método QueryDef.Cancel (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Cancelar

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync). **Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.

