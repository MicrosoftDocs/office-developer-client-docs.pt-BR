---
title: Método Read-ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307669"
---
# <a name="read-method-ado"></a>Método Read (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Lê um número de bytes especificado de um objeto [Stream](stream-object-ado.md) binário.

## <a name="syntax"></a>Sintaxe

** = *Fluxo*de Variant. Leitura (*NumBytes* )

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*NumBytes* |Opcional. Um valor **Long** que especifica o número de bytes a serem lidos do arquivo ou o valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que é o padrão.|

## <a name="return-value"></a>Valor de retorno

O método **Read** lê um número de bytes especificado ou o fluxo inteiro de um objeto **Stream** e retorna os dados resultantes como uma **Variant**.

## <a name="remarks"></a>Comentários

Se *NumBytes* for maior que o número de bytes restantes no **Stream**, apenas os bytes remanescentes serão retornados. Os dados lidos não serão enchidos para corresponder ao comprimento especificado por *NumBytes*. Se não houver bytes restantes a ler, uma variante com um valor nulo será retornada. **Read** não pode ser utilizado para ler de trás para frente.

> [!NOTE]
> *NumBytes* sempre mede bytes. Para objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**), utilize [ReadText](readtext-method-ado.md).


