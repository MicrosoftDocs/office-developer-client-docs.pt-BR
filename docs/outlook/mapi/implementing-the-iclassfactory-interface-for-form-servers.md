---
title: Implementando a Interface IClassFactory para servidores de formulário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767444"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="b4a46-103">Implementando a Interface IClassFactory para servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="b4a46-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="b4a46-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4a46-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4a46-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) é a interface OLE que aplicativos clientes usam para criar novos objetos de formulário da classe de mensagem do seu servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="b4a46-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="b4a46-106">A tabela a seguir lista os métodos de **IClassFactory** necessários.</span><span class="sxs-lookup"><span data-stu-id="b4a46-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="b4a46-107">**Method**</span><span class="sxs-lookup"><span data-stu-id="b4a46-107">**Method**</span></span>|<span data-ttu-id="b4a46-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b4a46-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4a46-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="b4a46-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="b4a46-110">Cria um novo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="b4a46-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="b4a46-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="b4a46-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="b4a46-112">Protege o servidor de formulário na memória para que possa ser evitada sobrecarga de inicialização quando vários objetos de formulário são criados.</span><span class="sxs-lookup"><span data-stu-id="b4a46-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="b4a46-113">Para todas as informações necessárias para implementar esses métodos, consulte a seção Serviços de objetos ActiveX e COM no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b4a46-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4a46-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a46-114">See also</span></span>



[<span data-ttu-id="b4a46-115">Escrevendo códigos de servidor do formulário</span><span class="sxs-lookup"><span data-stu-id="b4a46-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

