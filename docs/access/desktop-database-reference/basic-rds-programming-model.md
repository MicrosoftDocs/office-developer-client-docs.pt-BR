---
title: Modelo de programação básico do RDS
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717955"
---
# <a name="basic-rds-programming-model"></a>Modelo de programação básico do RDS

**Aplica-se a**: Access 2013, o Office 2013

O RDS lida com aplicativos existentes no seguinte ambiente: um aplicativo cliente especifica um programa a ser executado em um servidor e os parâmetros necessários para retornar as informações desejadas. O programa invocado no servidor obtém acesso à fonte de dados especificada, recupera as informações, talvez processe os dados e retorna as informações resultantes para o aplicativo cliente de modo que elas possam ser facilmente utilizadas. O RDS fornece os meios para realizar a seguinte sequência de ações:

- Especificar o programa a ser invocado no servidor e obter um modo de referir-se a ele a partir do cliente. (Essa referência é chamada, às vezes, de  *proxy*. Ela representa o programa do servidor remoto. O aplicativo cliente "chamará" o proxy como se fosse um programa local, mas, na verdade, ele invocará o programa do servidor remoto.)

- Invocar o programa do servidor. Passar parâmetros ao programa do servidor que identifiquem a fonte de dados e o comando a ser lançado. (O programa do servidor usa o ADO para obter o acesso à fonte de dados. O ADO faz a conexão com um dos parâmetros fornecidos e depois lança o comando especificado em outro parâmetro.)

- O programa do servidor obtém um objeto [Recordset](recordset-object-ado.md) da fonte de dados. Opcionalmente, o objeto **Recordset** é processado no servidor.

- O programa do servidor retorna o objeto **Recordset** final para o aplicativo cliente.

- No cliente, o objeto **Recordset** é colocado em um formato no qual ela possa ser facilmente utilizado por controles visuais.

- Quaisquer modificações no objeto **Recordset** são retornadas para o programa do servidor que as usa para atualizar a fonte de dados.

Esse modelo de programação contém determinados recursos de conveniência. Se você não precisar de um programa de servidor complexo para acessar a fonte de dados e fornecer os parâmetros de conexão e comando necessários, o RDS recuperará automaticamente os dados especificados com um programa de servidor padrão simples.

Se precisar de processamento mais complexo, você poderá especificar seu próprio programa de servidor personalizado. Por exemplo, como um programa de servidor tem todo o poder do ADO à sua disposição, ele poderia conectar-se a diversas fontes de dados diferentes, combinar seus dados de um modo complexo e, depois, retornar um resultado processado simples para o aplicativo cliente.

Finalmente, se suas necessidades estiverem no meio do caminho, o ADO agora oferece suporte à personalização do comportamento do programa de servidor padrão.

