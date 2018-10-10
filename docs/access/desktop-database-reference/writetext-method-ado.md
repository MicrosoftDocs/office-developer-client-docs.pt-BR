---
title: Método WriteText (ADO)
TOCTitle: WriteText Method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67dcf218814f938c4583ba9587085cff73066dc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465366"
---
# <a name="writetext-method-ado"></a>Método WriteText (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Grava uma sequência de texto especificada em um objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. WriteText*dados*, *Opções*

## <a name="parameters"></a>Parâmetros

  - *Data*

  - Um valor **String** que contém o texto em caracteres a ser gravado.

  - *Options*

  - Opcional. Um valor [StreamWriteEnum](streamwriteenum.md) que especifica se um caractere separador de linha deve ser gravado no final da sequência especificada.

## <a name="remarks"></a>Comentários

As sequências especificadas são gravadas no objeto **Stream** sem nenhum espaço ou caractere intermediário entre cada sequência.

A [Position](position-property-ado.md) atual será definida para o caractere que segue os dados gravados. O método **WriteText** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses caracteres, chame [SetEOS](seteos-method-ado.md).

Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de **Stream** será incrementado para conter quaisquer caracteres novos e **EOS** será movido para o último novo byte em **Stream**.


> [!NOTE]
> <P>O método <STRONG>WriteText</STRONG> é utilizado com fluxos de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>). Para fluxos binários (<STRONG>Type</STRONG> é <STRONG>adTypeBinary</STRONG>), utilize <A href="write-method-ado.md">Write</A>.</P>


