---
title: Visão geral do objeto Command
TOCTitle: Command object overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c7697d4ae8b830afb53eee10e7dd59a7dc8db4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296161"
---
# <a name="command-object-overview"></a>Visão geral do objeto Command

**Aplica-se ao:** Access 2013, Office 2013

Com as coleções, os métodos e as propriedades de um objeto **Command**, você pode fazer o que segue:

  - Definir o texto executável do comando (por exemplo, uma instrução SQL ou um procedimento armazenado) usando a propriedade **CommandText**.

  - Definir consultas com parâmetros ou argumentos de procedimentos armazenados usando objetos **Parameter** e a coleção **Parameters**.

  - Executar um comando e retornar um objeto **Recordset**, se adequado, usando o método **Execute**.

  - Especificar o tipo de comando usando a propriedade **CommandType** antes da execução, para otimizar o desempenho.

  - Controlar se o provedor salva uma versão preparada (ou compilada) do comando antes da execução usando a propriedade **Prepared**.

  - Definir o número de segundos que um provedor irá aguardar até a execução de um comando usando a propriedade **CommandTimeout**.

  - Associar uma conexão aberta a um objeto **Command** definindo sua propriedade **ActiveConnection**.

  - Definir a propriedade **Name** para identificar o objeto **Command** como um método no objeto **Connection** associado.

  - Passar um objeto **Command** para a propriedade **Source** de um **Recordset** para obter dados.

