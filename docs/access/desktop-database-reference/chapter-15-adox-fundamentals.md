---
title: 'Capítulo 15: Conceitos básicos do ADOX'
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296448"
---
# <a name="chapter-15-adox-fundamentals"></a>Capítulo 15: Conceitos básicos do ADOX

**Aplica-se ao:** Access 2013, Office 2013

O Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) é uma extensão dos objetos do ADO e do modelo de programação. O ADOX contém objetos para a criação e modificação de esquemas, bem como para segurança. Como ele consiste em uma abordagem baseada em objetos para a manipulação de esquemas, você pode criar um código a ser utilizado com várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.

O ADOX é uma biblioteca que acompanha os principais objetos do ADO. Ele apresenta objetos adicionais para a criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, contém objetos de segurança para manter usuários e grupos, bem como para conceder e revogar permissões em objetos.

Para usar o ADOX com a sua ferramenta de desenvolvimento, você deve estabelecer uma referência para a biblioteca de tipos do ADOX. A descrição da biblioteca do ADOX é "Ext. do Microsoft ADO para DDL e segurança". O nome do arquivo de biblioteca do ADOX é Msadox.dll, e a identificação do programa (ProgID) é "ADOX". Para obter mais informações sobre como estabelecer referências com as bibliotecas, consulte a documentação da sua ferramenta de desenvolvimento.

O Microsoft OLE DB Provider para o mecanismo de banco de dados Microsoft Jet oferece suporte completo para o ADOX. Certos recursos do ADOX podem não ter suporte, dependendo do seu provedor de dados. Para obter mais informações sobre os recursos para os quais há suporte com o Microsoft OLE DB Provider for ODBC, o Microsoft OLE DB Provider for Oracle ou o Microsoft OLE DB Provider for SQL Server, consulte o arquivo leia-me do MDAC.

Este documento pressupõe um conhecimento funcional da linguagem de programação Microsoft Visual Basic e um conhecimento geral do ADO. Para obter mais informações sobre o ADO, consulte o [Guia do programador do ADO](ado-programmer-s-guide.md).

Este capítulo aborda o tópico a seguir:

- [Suporte do provedor para ADOX](provider-support-for-adox.md)

Para obter mais informações gerais sobre o ADOX, consulte os seguintes tópicos:

- [Objetos do ADOX](adox-objects.md)
- [Coleções do ADOX](adox-collections.md)
- [Propriedades do ADOX](adox-properties.md)
- [Métodos do ADOX](adox-methods.md)
- [Exemplos de ADOX](adox-code-examples.md)

