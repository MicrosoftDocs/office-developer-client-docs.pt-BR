---
title: Propriedade canônica PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341591"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="7ec34-103">Propriedade canônica PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="7ec34-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="7ec34-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ec34-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ec34-105">Habilita a autenticação Kerberos de uma configuração de perfil.</span><span class="sxs-lookup"><span data-stu-id="7ec34-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="7ec34-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="7ec34-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ec34-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="7ec34-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="7ec34-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="7ec34-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ec34-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="7ec34-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="7ec34-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="7ec34-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ec34-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7ec34-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7ec34-112">Área:</span><span class="sxs-lookup"><span data-stu-id="7ec34-112">Area:</span></span>  <br/> |<span data-ttu-id="7ec34-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec34-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ec34-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ec34-114">Remarks</span></span>

<span data-ttu-id="7ec34-115">A definição dessa propriedade com o Nome de Domínio do servidor de diretório do usuário permite a conexão direta com o Controlador de Domínio (DC), que é necessário para um perfil que tenha sido configurado para usar a autenticação Kerberos no Microsoft Exchange Server 2007 e em versões anteriores, definindo o **RPC_C_AUTHN_GSS_KERBEROS** em **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="7ec34-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7ec34-116">O Microsoft Exchange Server 2010 e o Exchange Server 2013 lidam com chamadas do livro de endereços feitas ao Servidor de Acesso para Cliente de maneira diferente da maneira como o Exchange Server 2007 e versões anteriores as lidam.</span><span class="sxs-lookup"><span data-stu-id="7ec34-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="7ec34-117">O processo DSProxy não é mais usado, portanto, a autenticação Kerberos pode ter êxito.</span><span class="sxs-lookup"><span data-stu-id="7ec34-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="7ec34-118">No entanto, o cliente ainda estaria se comunicando com o servidor Exchange em  vez de diretamente com o DC, o que pode não ser desejado: a configuração PR_PROFILE_HOME_SERVER_FQDN evita isso.</span><span class="sxs-lookup"><span data-stu-id="7ec34-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7ec34-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ec34-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ec34-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="7ec34-120">Protocol specifications</span></span>

<span data-ttu-id="7ec34-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ec34-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ec34-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="7ec34-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ec34-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ec34-123">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ec34-124">Especifica operações permitidas para os objetos principais do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="7ec34-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ec34-125">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="7ec34-125">Header files</span></span>

<span data-ttu-id="7ec34-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ec34-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ec34-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="7ec34-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ec34-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ec34-128">Mapitags.h</span></span>
  
> <span data-ttu-id="7ec34-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="7ec34-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ec34-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ec34-130">See also</span></span>



[<span data-ttu-id="7ec34-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec34-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ec34-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec34-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ec34-133">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="7ec34-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ec34-134">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="7ec34-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

