---
title: Propriedade DBEngine. defaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294355"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="244e4-102">Propriedade DBEngine. defaultPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="244e4-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="244e4-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="244e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="244e4-104">Define a senha utilizada para criar o **Workspace** padrão quando ele é inicializado.</span><span class="sxs-lookup"><span data-stu-id="244e4-104">Sets the password used to create the default **Workspace** when it is initialized.</span></span> <span data-ttu-id="244e4-105">**String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="244e4-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="244e4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="244e4-106">Syntax</span></span>

<span data-ttu-id="244e4-107">*expressão* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="244e4-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="244e4-108">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="244e4-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="244e4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="244e4-109">Remarks</span></span>

<span data-ttu-id="244e4-p102">A configuração para **DefaultPassword** é um tipo de dados de cadeia de caracteres que pode conter até 20 caracteres. Ele pode conter qualquer caractere exceto ASCII 0.</span><span class="sxs-lookup"><span data-stu-id="244e4-p102">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="244e4-p103">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="244e4-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="244e4-117">Por padrão, a propriedade **DefaultUser** é definida como "admin" e a propriedade **DefaultPassword** é definida como uma sequência de comprimento zero ("").</span><span class="sxs-lookup"><span data-stu-id="244e4-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="244e4-p104">Normalmente, use o método **CreateWorkspace** para criar um objeto **Workspace** com um determinado nome de usuário e senha. Entretanto, para compatibilidade com versões anteriores e para sua conveniência, quando você não implementa um banco de dados seguro, o mecanismo de banco de dados do Microsoft Access cria automaticamente um objeto **Workspace** padrão se um ainda não foi aberto. Nesse caso, os valores das propriedades **DefaultUser** e **DefaultPassword** definem o usuário e a senha para o objeto **Workspace** padrão.</span><span class="sxs-lookup"><span data-stu-id="244e4-p104">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="244e4-121">Para essa propriedade ser efetivada, você deve defini-la antes de chamar quaisquer métodos DAO.</span><span class="sxs-lookup"><span data-stu-id="244e4-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

