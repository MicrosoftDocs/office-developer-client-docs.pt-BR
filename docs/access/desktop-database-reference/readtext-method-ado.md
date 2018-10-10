---
title: Método ReadText (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a44a3a002d390879e5d56d9c6931a91cba40271
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461986"
---
# <a name="readtext-method-ado"></a>Método ReadText (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Lê o número de caracteres especificado de um objeto [Stream](stream-object-ado.md) de texto.

## <a name="syntax"></a>Sintaxe

*Cadeia de caracteres* = *Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Parâmetros

  - *NumChars*

  - Opcional. Um valor **Long** que especifica o número de caracteres a serem lidos do arquivo ou um valor [StreamReadEnum](streamreadenum.md). O valor padrão é **adReadAll**.

## <a name="return-value"></a>Valor de Retorno

O método **ReadText** lê um número de caracteres especificado, uma linha inteira ou o fluxo inteiro a partir de um objeto **Stream** e retorna a sequência resultante.

## <a name="remarks"></a>Comentários

Se *NumChar* for maior que o número de caracteres restantes no fluxo, apenas os caracteres remanescentes serão retornados. A sequência lida não será enchida para corresponder ao comprimento especificado por *NumChar*. Se não houver caracteres restantes a ler, uma variante cujo valor é nulo será retornada. **ReadText** não pode ser utilizado para ler de trás para frente.


> [!NOTE]
> <P>O método <STRONG>ReadText</STRONG> é utilizado com fluxos de texto (<A href="type-property-ado-stream.md">Type</A> é <STRONG>adTypeText</STRONG>). Para fluxos binários (<STRONG>Type</STRONG> é <STRONG>adTypeBinary</STRONG>), utilize <A href="read-method-ado.md">Read</A>.</P>


