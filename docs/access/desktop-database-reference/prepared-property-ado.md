---
title: Propriedade Prepared (ADO)
TOCTitle: Prepared Property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865453f89cd5942ec7f9f8d036beb72dc519397e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462248"
---
# <a name="prepared-property-ado"></a>Propriedade Prepared (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica se uma versão compilada de um comando deve ser salva antes da execução.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Boolean** que, se definido como **True**, indicará que o comando deve ser preparado.

## <a name="remarks"></a>Comentários

Utilize a propriedade **Prepared** para que o provedor salve uma versão preparada (ou compilada) da consulta especificada na propriedade [CommandText](commandtext-property-ado.md) antes da primeira execução de um objeto [Command](command-object-ado.md). Isto pode fazer com que a primeira execução do comando demore, mas depois que o provedor compilar um comando, ele utilizará a versão compilada do comando para quaisquer execuções subsequentes, melhorando o desempenho.

Se a propriedade for **False**, o provedor executará o objeto **Command** diretamente sem criar uma versão compilada.

Se o provedor não oferecer suporte à preparação do comando, ele poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, ele simplesmente ignorará a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.

