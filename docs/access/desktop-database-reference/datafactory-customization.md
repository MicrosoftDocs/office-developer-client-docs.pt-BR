---
title: Personalização de DataFactory
TOCTitle: DataFactory Customization
ms:assetid: 43cd7416-1f05-87ee-22f0-6cf0d2d1b39f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249205(v=office.15)
ms:contentKeyID: 48544511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a7ddd728908212716256eaa65adc925548e739e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879699"
---
# <a name="datafactory-customization"></a>Personalização de DataFactory


**Aplica-se a**: Access 2013, o Office 2013

O RDS (Remote Data Service) oferece uma forma de acesso fácil aos dados em um sistema cliente/servidor de três camadas. Um controle de dados de cliente especifica os parâmetros da sequência de conexão e da sequência de comando para executar uma consulta em uma fonte de dados remota, ou parâmetros da sequência de conexão e do objeto [Recordset](recordset-object-ado.md) para executar uma atualização.

Os parâmetros são passados para um programa de servidor, que executa a operação de acesso a dados na fonte de dados remota. O RDS disponibiliza um programa de servidor padrão, o objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md). O objeto **RDSServer.DataFactory** retorna qualquer objeto **Recordset** produzido por uma consulta ao cliente.

Entretanto, o **RDSServer.DataFactory** limita-se à realização de consultas e atualizações. Ele não pode executar qualquer validação ou processamento nas sequência de comando ou de conexão.

Com o ADO, você pode especificar o funcionamento de **DataFactory** em conjunto com outro tipo de programa de servidor, denominado *manipulador*. O manipulador pode modificar as sequências de comando e de conexão do cliente antes de elas serem usadas para acessar a fonte de dados. Ele também pode impor direitos de acesso, que permitem que o cliente leia e grave dados na fonte de dados.

Os parâmetros usados pelo manipulador para modificar parâmetros de cliente e direitos de acesso são especificados nas seções de um arquivo de personalização.

Consulte os tópicos a seguir para obter mais informações sobre como personalizar o objeto **DataFactory**:

  - [Noções básicas sobre o arquivo de personalização](understanding-the-customization-file.md)

  - [Seção connect do arquivo de personalização](customization-file-connect-section.md)

  - [Seção SQL do arquivo de personalização](customization-file-sql-section.md)

  - [Seção userlist do arquivo de personalização](customization-file-userlist-section.md)

  - [Seção logs do arquivo de personalização](customization-file-logs-section.md)

  - [Configurações necessárias do cliente](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/required-client-settings)

  - [Criando seu próprio manipulador personalizado](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/writing-your-own-customized-handler)
