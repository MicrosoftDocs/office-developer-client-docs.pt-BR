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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308586"
---
# <a name="specifying-threads-per-processor-on-iis"></a>Especificação de threads por processador no IIS


**Aplica-se ao:** Access 2013, Office 2013

Ao usar o RDS com os serviços de informações da Internet 4,0 ou posterior, o número de threads criados por processador pode ser controlado pela manipulação do registro no servidor Web. O número de encadeamentos por processador pode afetar o desempenho em uma situação de alto tráfego ou em situações de baixo tráfego em consultas de maior tamanho. O usuário deve experimentar para melhores resultados.

O método usado para determinar e alterar o valor padrão para essa definição depende da configuração do servidor IIS 4.0.

Com o MDAC 2.1.2.4202.3 (GA) ou posterior instalado no IIS, o RDS usa o mesmo pool de encadeamento Component Services (ou Microsoft Transaction Services, se você estiver usando o Windows NT) usado pelos scripts ASP. O valor padrão para o número de encadeamentos por processador é 10. Para alterar o padrão, você deve incluir a seguinte chave para o registro do servidor:

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

em que *MaxPoolThreads* é um\_reg DWORD. *MaxPoolThreads* não aparece no Registro, a menos que seja especificamente adicionado. Os valores válidos variam de 5 a um máximo recomendado de 20. Se o valor especificado pela chave de registro for superior ao valor da chave *PoolThreadLimit* (localizada no mesmo caminho), será usado o valor *PoolThreadLimit*.

Como alternativa, se o MDAC 2.1 2.1.1.3711.11 (GA) ou anterior estiver instalado no servidor IIS, o valor padrão para o número de encadeamentos por processador será 6. Para alterar o padrão, você deve incluir a seguinte chave no registro do servidor IIS:

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

em que *ADCThreads* é um\_reg DWORD. O *ADCThreads* não aparece no Registro a menos que seja especificamente adicionado. O intervalo de valores válidos é de 1 a 50. Se o valor especificado pela chave de registro for superior a 50, o valor máximo será usado (50).

