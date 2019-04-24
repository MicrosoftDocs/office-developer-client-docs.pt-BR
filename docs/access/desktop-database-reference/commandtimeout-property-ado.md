---
title: Propriedade CommandTimeout (ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296126"
---
# <a name="commandtimeout-property-ado"></a>Propriedade CommandTimeout (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica quanto tempo esperar durante a execução de um comando antes de interromper a tentativa e gerar um erro.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que um comando seja executado. O padrão é 30.

## <a name="remarks"></a>Comentários

Use a propriedade **CommandTimeout** em um objeto [Connection](connection-object-ado.md) ou [Command](command-object-ado.md) para permitir o cancelamento de uma chamada do método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) devido a atrasos no tráfego da rede ou uso intenso do servidor. Se o intervalo definido na propriedade **CommandTimeout** terminar antes de o comando concluir a execução, um erro será gerado e o ADO cancelará o comando. Se você definir a propriedade como zero, o ADO aguardará indefinidamente até que a execução seja concluída. Verifique se o provedor e a fonte de dados na qual está escrevendo o código oferecem suporte à funcionalidade **CommandTimeout**.

A definição de **CommandTimeout** em um objeto **Connection** não afeta a definição de **CommandTimeout** em um objeto **Command** no mesmo objeto **Connection**; isto é, a propriedade **CommandTimeout** do objeto **Command** não herda o valor de **CommandTimeout** do objeto **Connection**.

Em um objeto **Connection**, a propriedade **CommandTimeout** continua sendo de leitura/gravação depois que **Connection** é aberto.

