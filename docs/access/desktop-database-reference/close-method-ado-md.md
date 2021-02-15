---
title: Método Close (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296315"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="c50c5-102">Método Close (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c50c5-102">Close method (ADO MD)</span></span>


<span data-ttu-id="c50c5-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c50c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c50c5-104">Fecha um conjunto de células aberto.</span><span class="sxs-lookup"><span data-stu-id="c50c5-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50c5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c50c5-105">Syntax</span></span>

<span data-ttu-id="c50c5-106">*Cellset*. Fechar</span><span class="sxs-lookup"><span data-stu-id="c50c5-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="c50c5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="c50c5-107">Remarks</span></span>

<span data-ttu-id="c50c5-p101">O uso do método **Close** para fechar o objeto [Cellset](cellset-object-ado-md.md) liberará os dados associados, incluindo dados em objetos [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) ou [Member](member-object-ado-md.md) relacionados. O fechamento de **Cellset** não o remove da memória; você pode alterar suas configurações de propriedade e abri-lo novamente mais tarde. Para eliminar totalmente um objeto da memória, defina a variável de objeto como **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="c50c5-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="c50c5-p102">Posteriormente, você poderá chamar o método [Open](open-method-ado-md.md) para reabrir o **Cellset** usando a mesma cadeia de caracteres de origem ou outra. Enquanto o objeto **Cellset** estiver fechado, será gerado um erro durante a recuperação de propriedades ou a chamada de métodos que façam referência aos dados ou metadados subjacentes.</span><span class="sxs-lookup"><span data-stu-id="c50c5-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

