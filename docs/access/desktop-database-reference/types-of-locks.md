---
title: Tipos de bloqueios (referência de banco de dados do Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314158"
---
# <a name="types-of-locks"></a><span data-ttu-id="3f4a1-102">Tipos de bloqueio</span><span class="sxs-lookup"><span data-stu-id="3f4a1-102">Types of locks</span></span>


<span data-ttu-id="3f4a1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f4a1-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="3f4a1-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="3f4a1-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="3f4a1-p101">Indica atualizações de lotes otimistas. Necessário para o modo de atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span>

<span data-ttu-id="3f4a1-p102">Muitos aplicativos buscam um número de linhas e depois precisam fazer atualizações coordenadas que incluem todo o conjunto de linhas a ser inserido, atualizado ou excluído. Com os cursores em lote, é necessária apenas uma viagem de ida e volta ao servidor, aprimorando o desempenho e diminuindo o tráfego de rede. Usando uma biblioteca de cursores em lote, você pode criar um cursor estático e desconectar-se da fonte de dados. Nesse momento, será possível fazer alterações nas linhas e, consequentemente, refazer a conexão e enviar as alterações para a fonte de dados de um lote.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-p102">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted. With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic. Using a batch cursor library, you can create a static cursor and then disconnect from the data source. At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="3f4a1-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="3f4a1-111">adLockOptimistic</span></span>

<span data-ttu-id="3f4a1-p103">Indica que o provedor usa bloqueio otimista — bloqueando registros apenas quando você chama o método **Update**. Isso significa que existe uma possibilidade de os dados serem alterados por outro usuário entre o tempo em que você edita o registro e chama o **Update**, o que criará conflitos. Use esse tipo de bloqueio em situações em que as possibilidades de choque sejam baixas ou em que eles possam ser prontamente resolvidos.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-p103">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method. This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts. Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="3f4a1-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="3f4a1-115">adLockPessimistic</span></span>

<span data-ttu-id="3f4a1-p104">Indica bloqueio pessimista, registro por registro. O provedor faz o que é necessário para garantir a edição bem-sucedida de registros, normalmente bloqueando registros na fonte de dados imediatamente antes da edição. Evidentemente, isso significa que os registros ficam indisponíveis para outros usuários quando você começa a editar, até que você libere o bloqueio chamando  **Update.** Use esse tipo de bloqueio em um sistema em que não é possível manter alterações concorrentes de dados, como em um sistema reserva.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-p104">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing. Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.** Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="3f4a1-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="3f4a1-120">adLockReadOnly</span></span>

<span data-ttu-id="3f4a1-p105">Indica registros somente leitura. Não é possível alterar dados. Um bloqueio somente leitura é o tipo mais "rápido" de bloqueio, pois não requer que o servidor mantenha um bloqueio nos registros.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-p105">Indicates read-only records. You cannot alter the data. A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="3f4a1-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="3f4a1-124">adLockUnspecified</span></span>

<span data-ttu-id="3f4a1-125">Não especifica um tipo de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3f4a1-125">Does not specify a type of lock.</span></span>

