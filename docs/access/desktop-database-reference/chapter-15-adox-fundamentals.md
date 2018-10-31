---
title: 'Capítulo 15: Conceitos básicos do ADOX'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 362fd0784ee596852af7b16fae5636330a52ed59
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863742"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="737bc-102">Capítulo 15: Conceitos básicos do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="737bc-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="737bc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="737bc-p101">O ADOX (Extensões do Microsoft® ActiveX® Data Objects para linguagem de definição de dados e segurança) é uma extensão do modelo de objetos e programação do ADO. O ADOX inclui objetos para criação e modificação de esquemas, bem como para segurança. Por ser uma manipulação da abordagem do esquema baseada em objeto, é possível escrever código que funcionará em várias fontes de dados, independentemente das diferenças em suas sintaxes nativas.</span><span class="sxs-lookup"><span data-stu-id="737bc-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="737bc-p102">O ADOX é uma biblioteca associada aos objetos básicos do ADO. Ele expõe objetos adicionais para criação, modificação e exclusão de objetos de esquema, como tabelas e procedimentos. Além disso, inclui objetos de segurança para manter os usuários e grupos e para conceder e revogar permissões nos objetos.</span><span class="sxs-lookup"><span data-stu-id="737bc-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="737bc-p103">Para usar o ADOX com a sua ferramenta de desenvolvimento, você deve estabelecer uma referência para a biblioteca de tipos do ADOX. A descrição da biblioteca do ADOX é "Ext. do Microsoft ADO para DDL e segurança". O nome do arquivo de biblioteca do ADOX é Msadox.dll, e a identificação do programa (ProgID) é "ADOX". Para obter mais informações sobre como estabelecer referências com as bibliotecas, consulte a documentação da sua ferramenta de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="737bc-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="737bc-p104">O Microsoft OLE DB Provider para o mecanismo de banco de dados Microsoft Jet oferece suporte completo para o ADOX. Certos recursos do ADOX podem não ter suporte, dependendo do seu provedor de dados. Para obter mais informações sobre os recursos para os quais há suporte com o Microsoft OLE DB Provider for ODBC, o Microsoft OLE DB Provider for Oracle ou o Microsoft OLE DB Provider for SQL Server, consulte o arquivo leia-me do MDAC.</span><span class="sxs-lookup"><span data-stu-id="737bc-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="737bc-117">Este documento considera que o usuário tenha conhecimento prático da linguagem de programação Microsoft® Visual Basic® e um conhecimento geral do ADO.</span><span class="sxs-lookup"><span data-stu-id="737bc-117">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO.</span></span> <span data-ttu-id="737bc-118">Para obter mais informações sobre o ADO, consulte o [Guia do Programador do ADO](ado-programmer-s-guide.md).</span><span class="sxs-lookup"><span data-stu-id="737bc-118">For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md).</span></span>

<span data-ttu-id="737bc-119">Este capítulo aborda o seguinte tópico:</span><span class="sxs-lookup"><span data-stu-id="737bc-119">This chapter covers the following topic:</span></span>

- [<span data-ttu-id="737bc-120">Suporte do provedor para ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-120">Provider Support for ADOX</span></span>](provider-support-for-adox.md)

<span data-ttu-id="737bc-121">Para obter mais informações gerais sobre o ADOX, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="737bc-121">For more overview information about ADOX, see the following topics:</span></span>

- [<span data-ttu-id="737bc-122">Objetos do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-122">ADOX Objects</span></span>](adox-objects.md)

- [<span data-ttu-id="737bc-123">Coleções do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-123">ADOX Collections</span></span>](adox-collections.md)

- [<span data-ttu-id="737bc-124">Propriedades do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-124">ADOX Properties</span></span>](adox-properties.md)

- [<span data-ttu-id="737bc-125">Métodos do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-125">ADOX Methods</span></span>](adox-methods.md)

- [<span data-ttu-id="737bc-126">Exemplos do ADOX</span><span class="sxs-lookup"><span data-stu-id="737bc-126">ADOX Examples</span></span>](adox-code-examples.md)

