---
title: Automação com o Microsoft Access
TOCTitle: Automation with Microsoft Access
description: O Microsoft Access é um componente COM que oferece suporte à Automação, anteriormente denominada Automação OLE.
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5104ab19c5fab816040d7a5d56fa6f425658c245
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874248"
---
# <a name="automation-with-microsoft-access"></a>Automação com o Microsoft Access

**Aplica-se a**: Access 2013, o Office 2013

O Microsoft Access é um componente COM que oferece suporte à Automação, anteriormente denominada Automação OLE. O Microsoft Access oferece suporte à Automação de duas maneiras. A partir do Microsoft Access, você pode trabalhar com objetos fornecidos por um outro componente. O Microsoft Access também fornece seus objetos a outros componentes COM.

Você pode usar a palavra-chave **New** ou o método **CreateObject** para criar uma nova instância de um componente. Use o método **GetObject** para atribuir uma variável a uma instância de um componente.

No Microsoft Access, você pode definir uma referência à biblioteca de tipos de um componente para melhorar o desempenho quando você trabalha com aquele componente através da Automação. O Microsoft Access também inclui o Pesquisador de objeto, uma ferramenta que permite que você veja objetos na biblioteca de tipos de um outro componente, bem como seus métodos e propriedades.

A biblioteca de tipos do Microsoft Access fornece informações sobre os objetos do Microsoft Access aos outros componentes. Você pode [definir uma referência](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) para o Microsoft Access digite biblioteca a partir de um componente e visualizar seus objetos no Pesquisador de objetos.

Para trabalhar com os objetos do Microsoft Access por meio da Automação, crie uma instância do objeto **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** do Microsoft Access. Por exemplo, suponha que você deseja exibir dados do Microsoft Excel em um formulário ou relatório do Microsoft Access. Para iniciar o Microsoft Access a partir do Microsoft Excel, use a palavra-chave **New** para criar uma instância do objeto **Application** do Microsoft Access. Também é possível usar o método **CreateObject** para criar uma nova instância do objeto **Application** do Microsoft Access ou usar o método **GetObject** para apontar uma variável de objeto para uma instância existente do Microsoft Access. Verifique a documentação do componente para determinar a qual sintaxe é oferecido suporte.

Depois de você ter iniciado uma instância do Microsoft Access, se você quiser controlar quaisquer objetos do Microsoft Access, você deve abrir um banco de dados ou projeto (. adp) na janela do Microsoft Access usando o **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** ou o **[NewCurrentDatabase ](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** método para um banco de dados ou usando o **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** ou o método **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** para um projeto.

Se você abriu o Microsoft Access somente como um meio de usando o Data Access Objects fornecidos pelo Microsoft DAO, você não precisará abrir um banco de dados na janela do Microsoft Access. Você pode usar a propriedade **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** do objeto de **aplicativo** do Microsoft Access para acessar objetos na biblioteca do Microsoft Office 12.0 Access banco de dados de mecanismo de objeto durante uma operação de automação.

