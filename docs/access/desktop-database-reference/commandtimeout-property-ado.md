---
title: Propriedade CommandTimeout (ADO)
TOCTitle: CommandTimeout Property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 58d95f6a3238d09ae10ddb3ba127a9fa68631f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462756"
---
# <a name="commandtimeout-property-ado"></a>Propriedade CommandTimeout (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica quanto tempo esperar durante a execução de um comando antes de interromper a tentativa e gerar um erro.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que um comando seja executado. O padrão é 30.

## <a name="remarks"></a>Comentários

Use a propriedade **CommandTimeout** em um objeto [Connection](connection-object-ado.md) ou [Command](command-object-ado.md) para permitir o cancelamento de uma chamada do método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) devido a atrasos no tráfego da rede ou uso intenso do servidor. Se o intervalo definido na propriedade **CommandTimeout** terminar antes de o comando concluir a execução, um erro será gerado e o ADO cancelará o comando. Se você definir a propriedade como zero, o ADO aguardará indefinidamente até que a execução seja concluída. Verifique se o provedor e a fonte de dados na qual está escrevendo o código oferecem suporte à funcionalidade **CommandTimeout**.

A definição de **CommandTimeout** em um objeto **Connection** não afeta a definição de **CommandTimeout** em um objeto **Command** no mesmo objeto **Connection**; isto é, a propriedade **CommandTimeout** do objeto **Command** não herda o valor de **CommandTimeout** do objeto **Connection**.

Em um objeto **Connection**, a propriedade **CommandTimeout** continua sendo de leitura/gravação depois que **Connection** é aberto.

