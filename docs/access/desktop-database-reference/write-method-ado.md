---
title: Método Write - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302461"
---
# <a name="write-method-ado"></a>Método Write (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Grava dados binários em um objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. Buffer de *Gravação*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Buffer* |Uma **Variant** que contém uma matriz de bytes a serem gravados.|

## <a name="remarks"></a>Comentários

Os bytes especificados são gravados no objeto **Stream** sem nenhum espaço intermediário entre cada byte.

A [Position](position-property-ado.md) atual será definida para o byte que segue os dados gravados. O método **Write** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).

Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de **Stream** será incrementado para conter quaisquer bytes novos e **EOS** será movido para o último novo byte em **Stream**.

> [!NOTE]
> O método **Write** é utilizado com fluxos binários ([Type](type-property-ado-stream.md) é **adTypeBinary**). Para fluxos de texto (**Type** é **adTypeText**), utilize [WriteText](writetext-method-ado.md).

