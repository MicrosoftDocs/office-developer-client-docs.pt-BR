---
title: O RDS retorna o erro "Stream não lido"
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 312d6f7e29a7573237bf8e4ddab17b9f8796cc4b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870013"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="2b993-102">RDS retorna \"Stream não lido\" erro</span><span class="sxs-lookup"><span data-stu-id="2b993-102">RDS Returns \"Stream Not Read\" Error</span></span>


<span data-ttu-id="2b993-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b993-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b993-p101">"O objeto Stream não pôde ser lido porque está vazio ou a posição atual está no final do Stream. Para Streams não vazios, defina a posição atual com a propriedade Position. Para determinar se um Stream está vazio, verifique a propriedade Size."</span><span class="sxs-lookup"><span data-stu-id="2b993-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="2b993-p102">Se você receber o erro acima, ele poderá ser o resultado de uma tentativa de uso de uma consulta hierárquica parametrizada por http. O RDS não permite que você mantenha hierarquias parametrizadas remotas.</span><span class="sxs-lookup"><span data-stu-id="2b993-p102">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http. RDS does not permit you to remote parameterized hierarchies.</span></span>

