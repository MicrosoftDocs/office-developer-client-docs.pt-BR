---
title: Propriedade preparado (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301453"
---
# <a name="prepared-property-ado"></a>Propriedade preparado (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica se uma versão compilada de um comando deve ser salva antes da execução.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Boolean** que, se definido como **True**, indicará que o comando deve ser preparado.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Prepared** para que o provedor salve uma versão preparada (ou compilada) da consulta especificada na propriedade [CommandText](commandtext-property-ado.md) antes da primeira execução de um objeto [Command](command-object-ado.md). Isto pode fazer com que a primeira execução do comando demore, mas depois que o provedor compilar um comando, ele utilizará a versão compilada do comando para quaisquer execuções subsequentes, melhorando o desempenho.

Se a propriedade for **False**, o provedor executará o objeto **Command** diretamente sem criar uma versão compilada.

Se o provedor não oferecer suporte à preparação do comando, ele poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, ele simplesmente ignorará a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.

