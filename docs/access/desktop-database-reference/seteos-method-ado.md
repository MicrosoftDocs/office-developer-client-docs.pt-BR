---
title: Método SetEOS (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f3b1ee81928a8da77cc3edff7f1feffb7196bba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722757"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="1ec6a-102">Método SetEOS (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ec6a-102">SetEOS method (ADO)</span></span>

<span data-ttu-id="1ec6a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ec6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ec6a-104">Define a posição que é o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1ec6a-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ec6a-105">Syntax</span></span>

<span data-ttu-id="1ec6a-106">*Stream*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="1ec6a-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec6a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ec6a-107">Remarks</span></span>

<span data-ttu-id="1ec6a-p101">**SetEOS** atualiza o valor da propriedade [EOS](eos-property-ado.md), tornando a [Posição](position-property-ado.md) atual o final do fluxo. Quaisquer bytes ou caracteres após a posição atual serão truncados.</span><span class="sxs-lookup"><span data-stu-id="1ec6a-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="1ec6a-110">Como [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) e [CopyTo](copyto-method-ado.md) não truncam nenhum valor extra nos objetos **Stream** existentes, você pode truncar esses bytes ou caracteres definindo a nova posição de final de fluxo com **SetEOS**.</span><span class="sxs-lookup"><span data-stu-id="1ec6a-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>

> [!WARNING]
> <span data-ttu-id="1ec6a-111">Se você definir **EOS** para uma posição antes do final real do fluxo, perderá todos os dados após a nova posição de **EOS**.</span><span class="sxs-lookup"><span data-stu-id="1ec6a-111">If you set **EOS** to a position before the actual end of the stream, you will lose all data after the new **EOS** position.</span></span>
