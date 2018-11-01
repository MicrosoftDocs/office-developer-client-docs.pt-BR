---
title: Propriedade ConnectionTimeout (ADO)
TOCTitle: ConnectionTimeout property (ADO)
ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15)
ms:contentKeyID: 48548589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab98e60e88a9685f138262a59a83f2b311c636da
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890929"
---
# <a name="connectiontimeout-property-ado"></a>Propriedade ConnectionTimeout (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica quanto tempo esperar ao estabelecer uma conexão antes de abortar a tentativa e gerar um erro.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long** que indica, em segundos, quanto tempo esperar para que a conexão seja aberta. O padrão é 15.

## <a name="remarks"></a>Comentários

Use a propriedade **ConnectionTimeout** em um objeto [Connection](connection-object-ado.md) se os atrasos no tráfego da rede ou o uso intenso do servidor tornarem necessário o abandono da tentativa de conexão. Se o tempo de definição da propriedade **ConnectionTimeout** terminar antes da abertura da conexão, um erro será gerado e o ADO cancelará a tentativa. Se você definir a propriedade como zero, o ADO esperará indefinidamente até que conexão seja aberta. Verifique se o provedor no qual você está escrevendo o código oferece suporte à funcionalidade **ConnectionTimeout**.

A propriedade **ConnectionTimeout** será leitura/gravação quando a conexão estiver fechada e somente leitura quando ela estiver aberta.

