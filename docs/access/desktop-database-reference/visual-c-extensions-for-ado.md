---
title: Extensões do Visual C++ para ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4e0d9e9f5db8741cb04fd4d576ea67408285aac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881759"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="13b9f-102">Extensões do Visual C++ para ADO</span><span class="sxs-lookup"><span data-stu-id="13b9f-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="13b9f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="13b9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="13b9f-104">O método preferencial de programação ADO com o Visual C++ está usando o \*\* \#importar\*\* diretiva, conforme discutido no [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span><span class="sxs-lookup"><span data-stu-id="13b9f-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="13b9f-105">Entretanto, as versões anteriores do ADO eram fornecidas com um método alternativo de programação utilizando o C++: as Extensões do Visual C++.</span><span class="sxs-lookup"><span data-stu-id="13b9f-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="13b9f-106">Esta seção documenta esse recurso para aqueles que deve manter o código de extensões do Visual C++, mas o novo código ADO deve ser escrito usando \# **Importar**.</span><span class="sxs-lookup"><span data-stu-id="13b9f-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="13b9f-p102">Um dos trabalhos mais tediosos que os programadores do Visual C++ enfrentam ao recuperar dados com o ADO é a conversão de dados retornados como um tipo de dados VARIANT em um tipo de dados C++ e, em seguida, o repositório dos dados convertidos em uma classe ou estrutura. Além de ser trabalhosa, a recuperação dos dados C++ por meio de tipo de dados VARIANT reduz o desempenho.</span><span class="sxs-lookup"><span data-stu-id="13b9f-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="13b9f-p103">O ADO fornece uma interface que oferece suporte à recuperação de dados em tipos de dados C/C++ nativos sem o uso de uma VARIANT, além de fornecer também macros pré-processadoras que simplificam o uso da interface. O resultado é uma ferramenta flexível, mais fácil de usar e com um excelente desempenho.</span><span class="sxs-lookup"><span data-stu-id="13b9f-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="13b9f-p104">Um cenário de cliente C/C++ comum é vincular um registro a um [Recordset](recordset-object-ado.md) para uma estrutura ou classe C/C++ contendo tipos nativos de C/C++. O uso de VARIANTs envolve a gravação do código de conversão da VARIANT para os tipos nativos de C/C++. As Extensões do Visual C++ para ADO visam facilitar esse cenário para o programador do Visual C++.</span><span class="sxs-lookup"><span data-stu-id="13b9f-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="13b9f-114">Consulte os tópicos a seguir para saber mais sobre as Extensões do Visual C++ para ADO.</span><span class="sxs-lookup"><span data-stu-id="13b9f-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="13b9f-115">Usando Extensões do Visual C++ para ADO</span><span class="sxs-lookup"><span data-stu-id="13b9f-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="13b9f-116">Cabeçalho das Extensões do Visual C++</span><span class="sxs-lookup"><span data-stu-id="13b9f-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="13b9f-117">ADO com exemplo de Extensões do Visual C++</span><span class="sxs-lookup"><span data-stu-id="13b9f-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

