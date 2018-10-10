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
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="e73db-102">Propriedades HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="e73db-102">HelpContext, HelpFile Properties (ADO)</span></span>


<span data-ttu-id="e73db-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e73db-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e73db-104">Indica o arquivo de ajuda e o tópico associado a um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e73db-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="e73db-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="e73db-105">Return Values</span></span>

  - <span data-ttu-id="e73db-106">**HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="e73db-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

  - <span data-ttu-id="e73db-107">**HelpFile**  retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="e73db-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e73db-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="e73db-108">Remarks</span></span>

<span data-ttu-id="e73db-p101">Se um arquivo de Ajuda for especificado na propriedade **HelpFile**, a propriedade **HelpContext** será usada para exibir automaticamente o tópico de Ajuda que ela identificar. Se não houver um tópico de ajuda relevante disponível, a propriedade **HelpContext** retornará zero e a propriedade **HelpFile** retornará uma sequência de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="e73db-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

