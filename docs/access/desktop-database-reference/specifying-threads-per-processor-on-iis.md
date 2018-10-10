---
title: Especificando encadeamentos por processador no IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de3c8c99c7f615928ea0a0f1e15171cc90b25f3d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462550"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Especificando encadeamentos por processador no IIS


**Aplica-se a**: Access 2013 | Office 2013

Ao utilizar o RDS com o Internet Information Services 4.0 ou posterior, o número de encadeamentos criados por processador pode ser controlado manipulando-se o registro no servidor da Web. O número de encadeamentos por processador pode afetar o desempenho em uma situação de alto tráfego ou em situações de baixo tráfego em consultas de maior tamanho. O usuário deve experimentar para melhores resultados.

O método usado para determinar e alterar o valor padrão para essa definição depende da configuração do servidor IIS 4.0.

Com o MDAC 2.1.2.4202.3 (GA) ou posterior instalado no IIS, o RDS usa o mesmo pool de encadeamento Component Services (ou Microsoft Transaction Services, se você estiver usando o Windows NT) usado pelos scripts ASP. O valor padrão para o número de encadeamentos por processador é 10. Para alterar o padrão, você deve incluir a seguinte chave para o registro do servidor:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

onde *MaxPoolThreads* é um REG\_DWORD. *MaxPoolThreads* não aparece no registro, a menos que especificamente, ela será adicionada. Os valores válidos variam de 5 a um máximo recomendado de 20. Se o valor especificado pela chave do registro for maior que o valor da chave *PoolThreadLimit* (localizada sob o mesmo caminho), o valor de *PoolThreadLimit* é usado.

Como alternativa, se o MDAC 2.1 2.1.1.3711.11 (GA) ou anterior estiver instalado no servidor IIS, o valor padrão para o número de encadeamentos por processador será 6. Para alterar o padrão, você deve incluir a seguinte chave no registro do servidor IIS:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

onde *ADCThreads* é um registro\_DWORD. *ADCThreads* não aparece no registro, a menos que especificamente, ela será adicionada. O intervalo de valores válidos é de 1 a 50. Se o valor especificado pela chave de registro for superior a 50, o valor máximo será usado (50).

