---
title: 'Capítulo 14: Conceitos básicos do ADO MD'
TOCTitle: 'Chapter 14: ADO MD fundamentals'
ms:assetid: 129baa54-0bc1-985d-4bfd-25a1c1c3018e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248899(v=office.15)
ms:contentKeyID: 48543346
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44a4e666fb615f7d3870acfbd986e93971606d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296462"
---
# <a name="chapter-14-ado-md-fundamentals"></a><span data-ttu-id="baae2-102">Capítulo 14: Conceitos básicos do ADO MD</span><span class="sxs-lookup"><span data-stu-id="baae2-102">Chapter 14: ADO MD fundamentals</span></span>

<span data-ttu-id="baae2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="baae2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="baae2-p101">O Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) oferece acesso fácil a dados multidimensionais de linguagens como Microsoft Visual Basic, Microsoft Visual C++ e Microsoft Visual J++. O ADO MD amplia o Microsoft ActiveX Data Objects (ADO) para incluir objetos específicos de dados multidimensionais, como os objetos [CubeDef](cubedef-object-ado-md.md) e [Cellset](cellset-object-ado-md.md). Com o ADO MD, você pode procurar esquemas multidimensionais, consultar um cubo e recuperar os resultados.</span><span class="sxs-lookup"><span data-stu-id="baae2-p101">Microsoft ActiveX Data Objects (Multidimensional) (ADO MD) provides easy access to multidimensional data from languages such as Microsoft Visual Basic, Microsoft Visual C++, and Microsoft Visual J++. ADO MD extends Microsoft ActiveX Data Objects (ADO) to include objects specific to multidimensional data, such as the [CubeDef](cubedef-object-ado-md.md) and [Cellset](cellset-object-ado-md.md) objects. With ADO MD you can browse multidimensional schema, query a cube, and retrieve the results.</span></span>

<span data-ttu-id="baae2-p102">Como o ADO, o ADO MD usa um provedor de OLE DB subjacente para obter acesso aos dados. Para utilizar o ADO MD, o provedor deve ser um MDP (provedor de dados multidimensionais), como definido na especificação do OLE DB para OLAP. Os MDPs apresentam dados em modos de exibição multidimensionais, ao contrário de TDPs (provedores de dados tabulares) que apresentam dados em modos de exibição tabulares. Consulte a documentação do provedor OLE DB para OLAP para obter informações mais detalhadas sobre a sintaxe e os comportamentos específicos aos quais seu provedor oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="baae2-p102">Like ADO, ADO MD uses an underlying OLE DB provider to gain access to data. To work with ADO MD, the provider must be a multidimensional data provider (MDP) as defined by the OLE DB for OLAP specification. MDPs present data in multidimensional views as opposed to tabular data providers (TDPs) that present data in tabular views. Refer to the documentation for your OLAP OLE DB provider for more detailed information on the specific syntax and behaviors supported by your provider.</span></span>

<span data-ttu-id="baae2-111">Este documento pressupõe que o usuário tenha experiência na linguagem de programação Visual Basic e conhecimento geral sobre ADO e OLAP.</span><span class="sxs-lookup"><span data-stu-id="baae2-111">This document assumes a working knowledge of the Visual Basic programming language and a general knowledge of ADO and OLAP.</span></span> <span data-ttu-id="baae2-112">Para obter mais informações, consulte o guia do programador [do ADO](ado-programmer-s-guide.md) e a Referência do programador OLE DB para OLAP Programmer's Reference.</span><span class="sxs-lookup"><span data-stu-id="baae2-112">For more information, see the [ADO programmer's guide](ado-programmer-s-guide.md) and the OLE DB for OLAP Programmer's Reference.</span></span> 

<span data-ttu-id="baae2-113">Este capítulo aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="baae2-113">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="baae2-114">Visão geral de dados e esquemas multidimensionais</span><span class="sxs-lookup"><span data-stu-id="baae2-114">Overview of multidimensional schemas and data</span></span>](overview-of-multidimensional-schemas-and-data.md)
- [<span data-ttu-id="baae2-115">Como trabalhar com dados multidimensionais</span><span class="sxs-lookup"><span data-stu-id="baae2-115">Working with multidimensional data</span></span>](working-with-multidimensional-data.md)
- [<span data-ttu-id="baae2-116">Usando o ADO com o ADO MD</span><span class="sxs-lookup"><span data-stu-id="baae2-116">Using ADO with ADO MD</span></span>](using-ado-with-ado-md.md)
- [<span data-ttu-id="baae2-117">Programando com o ADO MD</span><span class="sxs-lookup"><span data-stu-id="baae2-117">Programming with ADO MD</span></span>](programming-with-ado-md.md)
