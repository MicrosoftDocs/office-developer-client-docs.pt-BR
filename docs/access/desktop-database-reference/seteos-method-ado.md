---
title: Método SetEOS (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 456bbf7c7235d0db01b29372ee8f70c364263cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461952"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="d886b-102">Método SetEOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="d886b-102">SetEOS Method (ADO)</span></span>


<span data-ttu-id="d886b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d886b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d886b-104">Define a posição que é o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d886b-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d886b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d886b-105">Syntax</span></span>

<span data-ttu-id="d886b-106">*Stream*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="d886b-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="d886b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d886b-107">Remarks</span></span>

<span data-ttu-id="d886b-p101">**SetEOS** atualiza o valor da propriedade [EOS](eos-property-ado.md), tornando a [Posição](position-property-ado.md) atual o final do fluxo. Quaisquer bytes ou caracteres após a posição atual serão truncados.</span><span class="sxs-lookup"><span data-stu-id="d886b-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="d886b-110">Como [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) e [CopyTo](copyto-method-ado.md) não truncam nenhum valor extra nos objetos **Stream** existentes, você pode truncar esses bytes ou caracteres definindo a nova posição de final de fluxo com **SetEOS**.</span><span class="sxs-lookup"><span data-stu-id="d886b-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>


> [!WARNING]
> <P><span data-ttu-id="d886b-111">Se você definir <STRONG>EOS</STRONG> para uma posição antes do final real do fluxo, perderá todos os dados após a nova posição de <STRONG>EOS</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="d886b-111">If you set <STRONG>EOS</STRONG> to a position before the actual end of the stream, you will lose all data after the new <STRONG>EOS</STRONG> position.</span></span></P>


