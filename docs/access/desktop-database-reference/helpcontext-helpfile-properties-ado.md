---
title: Propriedades HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile Properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23823ec18b4b87306fa852ac5b0b18e89f60d057
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464647"
---
# <a name="helpcontext-helpfile-properties-ado"></a>Propriedades HelpContext, HelpFile (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o arquivo de ajuda e o tópico associado a um objeto [Error](error-object-ado.md).

## <a name="return-values"></a>Valores de retorno

  - **HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.

  - **HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.

## <a name="remarks"></a>Comentários

Se um arquivo de Ajuda for especificado na propriedade **HelpFile**, a propriedade **HelpContext** será usada para exibir automaticamente o tópico de Ajuda que ela identificar. Se não houver um tópico de ajuda relevante disponível, a propriedade **HelpContext** retornará zero e a propriedade **HelpFile** retornará uma sequência de comprimento zero ("").

