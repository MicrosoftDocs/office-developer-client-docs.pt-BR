---
title: Propriedade Charset (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703976"
---
# <a name="charset-property-ado"></a>Propriedade Charset (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica o conjunto de caracteres no qual o conteúdo de um texto [Stream](stream-object-ado.md) deve ser traduzido para armazenamento no buffer interno dos objetos Stream.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que especifica o conjunto de caracteres no qual o conteúdo do **Stream** será traduzido. O valor padrão é "Unicode". Os valores permitidos são sequências típicas passadas pela interface como sequências de conjuntos de caracteres para a Internet (por exemplo, "iso-8859-1", "Windows-1252" etc.). Para obter uma lista das sequências de conjunto de caracteres que é conhecida por um sistema, consulte as subchaves da HKEY\_CLASSES\_raiz\\MIME\\banco de dados\\Charset no registro do Windows.

## <a name="remarks"></a>Comentários

Em um objeto **Stream** de texto, os dados do texto são armazenados no conjunto de caracteres especificado pela propriedade **Charset**. O padrão é Unicode. A propriedade **Charset** é usada para a conversão de dados que entram no **Stream** ou saem do **Stream**. Por exemplo, se o **Stream** contiver dados ISO-8859-1 e estes forem copiados para um BSTR, o objeto **Stream** converterá os dados em Unicode. O inverso também é verdadeiro.

Para um **Stream** aberto, a propriedade [Position](position-property-ado.md) atual deve estar no começo do **Stream** (0) para que seja possível configurar **Charset**.

**Charset** é usada apenas com objetos **Stream** de texto ([Type](type-property-ado-stream.md) é **adTypeText**). Essa propriedade será ignorada se **Type** for **adTypeBinary**.

