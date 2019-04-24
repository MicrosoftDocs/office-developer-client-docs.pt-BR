---
title: Propriedade DBEngine. defaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294341"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="971c2-102">Propriedade DBEngine. defaultUser (DAO)</span><span class="sxs-lookup"><span data-stu-id="971c2-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="971c2-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="971c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="971c2-104">Define o nome de usuário utilizado para criar o **Workspace** padrão quando ele é inicializado.</span><span class="sxs-lookup"><span data-stu-id="971c2-104">Sets the user name used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="971c2-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="971c2-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="971c2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="971c2-106">Syntax</span></span>

<span data-ttu-id="971c2-107">*expressão* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="971c2-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="971c2-108">*expressão* Uma expressão que retorna um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="971c2-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="971c2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="971c2-109">Remarks</span></span>

<span data-ttu-id="971c2-110">A configuração para **DefaultUser** é um tipo de dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="971c2-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="971c2-111">Ele pode ter de 1 a 20 caracteres nos espaços de trabalho do Microsoft Access e pode incluir caracteres alfabéticos, caracteres acentuados, números, espaços e símbolos, exceto: "(aspas),/(barra \\ invertida), (barra invertida \[ \] ), (colchetes) ,: (dois pontos), | (pipe), \< (sinal de menor que), \> (sinal de maior que), + (sinal de mais), = (sinal de igual),; (ponto-e-vírgula),, (vírgula),?</span><span class="sxs-lookup"><span data-stu-id="971c2-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="971c2-112">(ponto de interrogação \* ), (asterisco), espaços à esquerda e caracteres de controle (ASCII 00 a ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="971c2-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="971c2-p103">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="971c2-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="971c2-118">Por padrão, a propriedade **DefaultUser** é definida como "admin" e a propriedade **DefaultPassword** é definida como uma sequência de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="971c2-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="971c2-p104">Os nomes de usuários normalmente não fazem distinção entre maiúsculas e minúsculas; contudo, se você estiver recriando uma conta de usuário que tenha sido excluída ou criada em um grupo de trabalho diferente, o nome do usuário deverá corresponder exatamente ao nome original, inclusive em relação à maiúsculas e minúsculas. As senhas fazem distinção entre maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="971c2-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="971c2-p105">Normalmente, use o método **CreateWorkspace** para criar um objeto **Workspace** com um determinado nome de usuário e senha. Entretanto, para compatibilidade com versões anteriores e para sua conveniência, quando você não implementa um banco de dados seguro, o mecanismo de banco de dados do Microsoft Access cria automaticamente um objeto **Workspace** padrão se um ainda não foi aberto. Nesse caso, os valores das propriedades **DefaultUser** e **DefaultPassword** definem o usuário e a senha para o objeto **Workspace** padrão.</span><span class="sxs-lookup"><span data-stu-id="971c2-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="971c2-124">Para essa propriedade ser efetivada, você deve defini-la antes de chamar quaisquer métodos DAO.</span><span class="sxs-lookup"><span data-stu-id="971c2-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

