---
title: Propriedade Recordset2.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307214"
---
# <a name="recordset2stillexecuting-property-dao"></a>Propriedade Recordset2.StillExecuting (DAO)


**Aplica-se ao:** Access 2013, Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . StillExecuting

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Use a propriedade **StillExecuting** para determinar se o método **Execute** ou **OpenConnection** chamado mais recentemente de forma assíncrona (ou seja, um método executado com a opção **dbRunAsync**) foi concluído. Enquanto a propriedade **StillExecuting** for **True**, qualquer objeto retornado não poderá ser acessado.

Assim que a propriedade **StillExecuting** retornar **False**, depois que a chamada **OpenConnection** retornar o objeto **Connection** associado, o objeto poderá ser mencionado. Contanto que **StillExecuting** permaneça **True**, o objeto poderá não ser mencionado, a não ser para ler a propriedade **StillExecuting**.

Use o método **[Cancel](connection-cancel-method-dao.md)** para concluir a execução de uma tarefa em andamento.

