---
title: Método Recordset2.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d3b943bed5abdd057b21e8a1380a68231d20e00
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463808"
---
# <a name="recordset2cancel-method-dao"></a>Método Recordset2.Cancel (DAO)


**Aplica-se a**: Access 2013 | Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . Cancelar

*expressão* Uma expressão que retorna um objeto **Recordset2** .

## <a name="remarks"></a>Comentários

Use o método **Cancel** para terminar a execução de uma chamada de método assíncrona **Execute** ou **OpenConnection** (ou seja, o método foi chamado com a opção dbRunAsync). **Cancelar** retornará um erro em tempo de execução se dbRunAsync não foi usada no método que você está tentando finalizar.

