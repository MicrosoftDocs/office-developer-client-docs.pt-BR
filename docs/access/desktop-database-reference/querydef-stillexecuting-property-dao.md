---
title: Propriedade QueryDef.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 62290944381687955b19e34f728e9ffff851bcd2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872820"
---
# <a name="querydefstillexecuting-property-dao"></a>Propriedade QueryDef.StillExecuting (DAO)


**Aplica-se a**: Access 2013, o Office 2013

## <a name="syntax"></a>Sintaxe

*expressão* . StillExecuting

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Use a propriedade **StillExecuting** para determinar se o método **[Execute](querydef-execute-method-dao.md)** ou **[OpenConnection](dbengine-openconnection-method-dao.md)** chamado mais recentemente de forma assíncrona (ou seja, um método executado com a opção **dbRunAsync**) foi concluído. Enquanto a propriedade **StillExecuting** for **True**, qualquer objeto retornado não poderá ser acessado.

Assim que a propriedade **StillExecuting** retornar **False**, depois que a chamada **OpenConnection** retornar o objeto **[Connection](connection-object-dao.md)** associado, o objeto poderá ser mencionado. Enquanto **StillExecuting** permanecer **True**, o objeto poderá não ser mencionado, a não ser para ler a propriedade **StillExecuting**.

Use o método **[Cancel](connection-cancel-method-dao.md)** para concluir a execução de uma tarefa em andamento.

