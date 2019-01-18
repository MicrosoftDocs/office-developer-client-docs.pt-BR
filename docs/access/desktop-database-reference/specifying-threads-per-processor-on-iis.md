---
title: Especificação de threads por processador no IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718179"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Especificação de threads por processador no IIS


**Aplica-se a**: Access 2013, o Office 2013

Ao usar o RDS com o Internet Information Services 4.0 ou posterior, o número de threads criados por processador pode ser controlado por manipulando o registro no servidor web. O número de encadeamentos por processador pode afetar o desempenho em uma situação de alto tráfego ou em situações de baixo tráfego em consultas de maior tamanho. O usuário deve experimentar para melhores resultados.

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

