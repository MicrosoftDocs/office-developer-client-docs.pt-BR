---
title: Escrever o método - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464720"
---
# <a name="write-method-ado"></a>Método Write (ADO)


**Aplica-se a**: Access 2013 | Office 2013


Grava dados binários em um objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Stream*. Gravar*Buffer*

## <a name="parameters"></a>Parâmetros

  - *Buffer*

  - Uma **Variant** que contém uma matriz de bytes a serem gravados.

## <a name="remarks"></a>Comentários

Os bytes especificados são gravados no objeto **Stream** sem nenhum espaço intermediário entre cada byte.

A [Position](position-property-ado.md) atual será definida para o byte que segue os dados gravados. O método **Write** não trunca o restante dos dados em um fluxo. Se você deseja truncar esses bytes, chame [SetEOS](seteos-method-ado.md).

Se você gravar após a posição [EOS](eos-property-ado.md) atual, o [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de **Stream** será incrementado para conter quaisquer bytes novos e **EOS** será movido para o último novo byte em **Stream**.


> [!NOTE]
> <P>O método <STRONG>Write</STRONG> é utilizado com fluxos binários (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeBinary</STRONG>). Para fluxos de texto (<STRONG>Type</STRONG> é <STRONG>adTypeText</STRONG>), utilize <A href="writetext-method-ado.md">WriteText</A>.</P>


