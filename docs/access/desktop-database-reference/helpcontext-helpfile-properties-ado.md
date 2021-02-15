---
title: Propriedades HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291989"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="04e22-102">Propriedades HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="04e22-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="04e22-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04e22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04e22-104">Indica o arquivo de ajuda e o tópico associado a um objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="04e22-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="04e22-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="04e22-105">Return values</span></span>

- <span data-ttu-id="04e22-106">**HelpContextID**  retorna uma ID de contexto, como um valor **Long**, para um tópico em um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="04e22-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="04e22-107">**HelpFile**  — retorna um valor **String** que avalia um caminho completamente resolvido para um arquivo de Ajuda.</span><span class="sxs-lookup"><span data-stu-id="04e22-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="04e22-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="04e22-108">Remarks</span></span>

<span data-ttu-id="04e22-p101">Se um arquivo de Ajuda for especificado na propriedade **HelpFile**, a propriedade **HelpContext** será usada para exibir automaticamente o tópico de Ajuda que ela identificar. Se não houver um tópico de ajuda relevante disponível, a propriedade **HelpContext** retornará zero e a propriedade **HelpFile** retornará uma sequência de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="04e22-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

