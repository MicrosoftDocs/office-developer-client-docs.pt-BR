---
title: Leia o método - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463132"
---
# <a name="read-method-ado"></a>Método Read (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Lê um número de bytes especificado de um objeto [Stream](stream-object-ado.md) binário.

## <a name="syntax"></a>Sintaxe

*Variant* = *Stream*. Leitura (*NumBytes* )

## <a name="parameters"></a>Parâmetros

  - *NumBytes*

  - Opcional. Um valor **Long** que especifica o número de bytes a serem lidos do arquivo ou o valor [adReadAll](streamreadenum.md) de **StreamReadEnum**, que é o padrão.

## <a name="return-value"></a>Valor de Retorno

O método **Read** lê um número de bytes especificado ou o fluxo inteiro de um objeto **Stream** e retorna os dados resultantes como uma **Variant**.

## <a name="remarks"></a>Comentários

Se *NumBytes* for maior que o número de bytes restantes no **Stream**, apenas os bytes remanescentes serão retornados. Os dados lidos não serão enchidos para corresponder ao comprimento especificado por *NumBytes*. Se não houver bytes restantes a ler, uma variante com um valor nulo será retornada. **Read** não pode ser utilizado para ler de trás para frente.


> [!NOTE]
> <P><EM>NumBytes</EM> sempre mede bytes. Para objetos <STRONG>Stream</STRONG> de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>), utilize <A href="readtext-method-ado.md">ReadText</A>.</P>


