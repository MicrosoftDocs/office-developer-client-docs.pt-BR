---
title: 'Capítulo 15: Conceitos básicos do ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72152a67a9846adacbc6b200a3517c7e65b9fc4c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881906"
---
# <a name="chapter-15-adox-fundamentals"></a>Capítulo 15: Conceitos básicos do ADOX


**Aplica-se a**: Access 2013, o Office 2013

O ADOX (Extensões do Microsoft® ActiveX® Data Objects para linguagem de definição de dados e segurança) é uma extensão do modelo de objetos e programação do ADO. O ADOX inclui objetos para criação e modificação de esquemas, bem como para segurança. Por ser uma manipulação da abordagem do esquema baseada em objeto, é possível escrever código que funcionará em várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.

O ADOX é uma biblioteca associada aos objetos básicos do ADO. Ele expõe objetos adicionais para criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, inclui objetos de segurança para manter os usuários e grupos e para conceder e revogar permissões nos objetos.

Para usar o ADOX com a sua ferramenta de desenvolvimento, você deve estabelecer uma referência para a biblioteca de tipos do ADOX. A descrição da biblioteca do ADOX é "Ext. do Microsoft ADO para DDL e segurança". O nome do arquivo de biblioteca do ADOX é Msadox.dll, e a identificação do programa (ProgID) é "ADOX". Para obter mais informações sobre como estabelecer referências com as bibliotecas, consulte a documentação da sua ferramenta de desenvolvimento.

O Microsoft OLE DB Provider para o mecanismo de banco de dados Microsoft Jet oferece suporte completo para o ADOX. Certos recursos do ADOX podem não ter suporte, dependendo do seu provedor de dados. Para obter mais informações sobre os recursos para os quais há suporte com o Microsoft OLE DB Provider for ODBC, o Microsoft OLE DB Provider for Oracle ou o Microsoft OLE DB Provider for SQL Server, consulte o arquivo leia-me do MDAC.

Este documento considera que o usuário tenha conhecimento prático da linguagem de programação Microsoft® Visual Basic® e um conhecimento geral do ADO. Para obter mais informações sobre o ADO, consulte o [Guia do Programador do ADO](ado-programmer-s-guide.md).

Este capítulo aborda o seguinte tópico:

- [Suporte do provedor para ADOX](provider-support-for-adox.md)

Para obter mais informações gerais sobre o ADOX, consulte os seguintes tópicos:

- [Objetos do ADOX](adox-objects.md)

- [Coleções do ADOX](adox-collections.md)

- [Propriedades do ADOX](adox-properties.md)

- [Métodos do ADOX](adox-methods.md)

- [Exemplos do ADOX](adox-code-examples.md)

