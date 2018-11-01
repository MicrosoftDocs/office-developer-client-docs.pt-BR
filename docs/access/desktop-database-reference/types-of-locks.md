---
title: Tipos de bloqueios (referência de banco de dados da área de trabalho do Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9aa0753892174995a8ffc0ee5901a86493f1349d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867507"
---
# <a name="types-of-locks"></a>Tipos de bloqueio


**Aplica-se a**: Access 2013, o Office 2013



## <a name="adlockbatchoptimistic"></a>adLockBatchOptimistic

Indica atualizações de lotes otimistas. Necessário para o modo de atualização em lote.

Muitos aplicativos buscam um número de linhas e depois precisam fazer atualizações coordenadas que incluem todo o conjunto de linhas a ser inserido, atualizado ou excluído. Com os cursores em lote, é necessária apenas uma viagem de ida e volta ao servidor, aprimorando o desempenho e diminuindo o tráfego de rede. Usando uma biblioteca de cursores em lote, você pode criar um cursor estático e desconectar-se da fonte de dados. Nesse momento, será possível fazer alterações nas linhas e, consequentemente, refazer a conexão e enviar as alterações para a fonte de dados de um lote.

## <a name="adlockoptimistic"></a>adLockOptimistic

Indica que o provedor usa bloqueio otimista  bloqueando registros apenas quando você chama o método **Update**. Isso significa que existe uma possibilidade de os dados serem alterados por outro usuário entre o tempo em que você edita o registro e chama o **Update**, o que criará conflitos. Use esse tipo de bloqueio em situações em que as possibilidades de choque sejam baixas ou em que eles possam ser prontamente resolvidos.

## <a name="adlockpessimistic"></a>adLockPessimistic

Indica bloqueio pessimista, registro por registro. O provedor faz o que é necessário para garantir a edição bem-sucedida de registros, normalmente bloqueando registros na fonte de dados imediatamente antes da edição. Evidentemente, isso significa que os registros ficam indisponíveis para outros usuários quando você começa a editar, até que você libere o bloqueio chamando **Update.** Use esse tipo de bloqueio em um sistema em que não é possível manter alterações concorrentes de dados, como em um sistema reserva.

## <a name="adlockreadonly"></a>adLockReadOnly

Indica registros somente leitura. Não é possível alterar dados. Um bloqueio somente leitura é o tipo mais "rápido" de bloqueio, pois não requer que o servidor mantenha um bloqueio nos registros.

## <a name="adlockunspecified"></a>adLockUnspecified

Não especifica um tipo de bloqueio.

