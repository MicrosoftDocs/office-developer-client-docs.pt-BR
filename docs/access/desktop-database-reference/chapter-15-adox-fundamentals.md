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
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="6f267-102">Capítulo 15: Conceitos básicos do ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-102">Chapter 15: ADOX fundamentals</span></span>

<span data-ttu-id="6f267-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f267-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f267-p101">O Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) é uma extensão dos objetos do ADO e do modelo de programação. O ADOX contém objetos para a criação e modificação de esquemas, bem como para segurança. Como ele consiste em uma abordagem baseada em objetos para a manipulação de esquemas, você pode criar um código a ser utilizado com várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.</span><span class="sxs-lookup"><span data-stu-id="6f267-p101">Microsoft ActiveX Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="6f267-p102">O ADOX é uma biblioteca que acompanha os principais objetos do ADO. Ele apresenta objetos adicionais para a criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, contém objetos de segurança para manter usuários e grupos, bem como para conceder e revogar permissões em objetos.</span><span class="sxs-lookup"><span data-stu-id="6f267-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="6f267-p103">Para usar o ADOX com a sua ferramenta de desenvolvimento, você deve estabelecer uma referência para a biblioteca de tipos do ADOX. A descrição da biblioteca do ADOX é "Ext. do Microsoft ADO para DDL e segurança". O nome do arquivo de biblioteca do ADOX é Msadox.dll, e a identificação do programa (ProgID) é "ADOX". Para obter mais informações sobre como estabelecer referências com as bibliotecas, consulte a documentação da sua ferramenta de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6f267-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="6f267-p104">O Microsoft OLE DB Provider para o mecanismo de banco de dados Microsoft Jet oferece suporte completo para o ADOX. Certos recursos do ADOX podem não ter suporte, dependendo do seu provedor de dados. Para obter mais informações sobre os recursos para os quais há suporte com o Microsoft OLE DB Provider for ODBC, o Microsoft OLE DB Provider for Oracle ou o Microsoft OLE DB Provider for SQL Server, consulte o arquivo leia-me do MDAC.</span><span class="sxs-lookup"><span data-stu-id="6f267-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="6f267-117">Este documento pressupõe um conhecimento funcional da linguagem de programação Microsoft Visual Basic e um conhecimento geral do ADO.</span><span class="sxs-lookup"><span data-stu-id="6f267-117">This document assumes a working knowledge of the Microsoft Visual Basic programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="6f267-118">Para obter mais informações sobre o ADO, consulte o [Guia do programador do ADO](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="6f267-118">For more information about ADO, see the [ADO programmer's guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="6f267-119">Este capítulo aborda o tópico a seguir:</span><span class="sxs-lookup"><span data-stu-id="6f267-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="6f267-120">Suporte do provedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-120">Provider support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="6f267-121">Para obter mais informações gerais sobre o ADOX, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6f267-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="6f267-122">Objetos do ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-122">ADOX objects</span></span>](adox-objects.md)
- [<span data-ttu-id="6f267-123">Coleções do ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-123">ADOX collections</span></span>](adox-collections.md)
- [<span data-ttu-id="6f267-124">Propriedades do ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-124">ADOX properties</span></span>](adox-properties.md)
- [<span data-ttu-id="6f267-125">Métodos do ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-125">ADOX methods</span></span>](adox-methods.md)
- [<span data-ttu-id="6f267-126">Exemplos de ADOX</span><span class="sxs-lookup"><span data-stu-id="6f267-126">ADOX examples</span></span>](adox-code-examples.md)

