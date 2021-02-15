---
title: Método WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308264"
---
# <a name="writetext-method-ado"></a>Método WriteText (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Grava uma sequência de texto especificada em um objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. Dados *WriteText*, *Opções*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Data* |Um valor **String** que contém o texto em caracteres a ser gravado.|
|*Options* |Opcional. Um valor [StreamWriteEnum](streamwriteenum.md) que especifica se um caractere separador de linha deve ser gravado no final da sequência especificada.|

## <a name="remarks"></a>Comentários

As sequências especificadas são gravadas no objeto **Stream** sem nenhum espaço ou caractere intermediário entre cada sequência.

A [Position](position-property-ado.md) atual será definida para o caractere que segue os dados gravados. O método **WriteText** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses caracteres, chame [SetEOS](seteos-method-ado.md).

Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de **Stream** será incrementado para conter quaisquer caracteres novos e **EOS** será movido para o último novo byte em **Stream**.

> [!NOTE]
> O método **WriteText** é utilizado com fluxos de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Para fluxos binários (**Type** é **adTypeBinary**), utilize [Write](write-method-ado.md).


