---
title: Método Recordset. Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300809"
---
# <a name="recordsetcancel-method-dao"></a>Método Recordset. Cancel (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Cancelar

*expressão* Uma variável que representa um objeto **Recordset** .

## <a name="remarks"></a>Comentários

Use o método **Cancel** para encerrar a execução de uma chamada de método **Execute** ou **OpenConnection** assíncrona (ou seja, o método foi invocado com a opção dbRunAsync). **Cancel** retornará um erro em tempo de execução se dbRunAsync não tiver sido usado no método que você está tentando encerrar.

