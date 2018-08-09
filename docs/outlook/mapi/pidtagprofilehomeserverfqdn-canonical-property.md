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
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769681"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="a2d3c-103">Propriedade canônica PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="a2d3c-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="a2d3c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2d3c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2d3c-105">Habilita a autenticação Kerberos de uma configuração de perfil.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="a2d3c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a2d3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a2d3c-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="a2d3c-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="a2d3c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a2d3c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a2d3c-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="a2d3c-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="a2d3c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a2d3c-110">Data type:</span></span>  <br/> |<span data-ttu-id="a2d3c-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2d3c-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a2d3c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a2d3c-112">Area:</span></span>  <br/> |<span data-ttu-id="a2d3c-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="a2d3c-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2d3c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2d3c-114">Remarks</span></span>

<span data-ttu-id="a2d3c-115">A definição dessa propriedade para o nome de domínio do servidor de diretório do usuário permite que a conexão direta para a Domain Controller (DC), que é necessário para um perfil que tenha sido configurado para usar a autenticação Kerberos em relação a Microsoft Exchange Server 2007 e nas versões anteriores, definindo **RPC_C_AUTHN_GSS_KERBEROS** em **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a2d3c-116">Microsoft Exchange Server 2010 e Exchange Server 2013 lidar com chamadas de catálogo de endereços feitas ao servidor de acesso de cliente forma diferente a partir da maneira em que o Exchange Server 2007 e versões anteriores-los pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="a2d3c-117">O processo de DSProxy não é mais usado, portanto a autenticação Kerberos talvez tenham êxito.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="a2d3c-118">No entanto, o cliente ainda seria se comunicar com o Exchange server, em vez de diretamente com o controlador de domínio, não pode ser desejável: configuração **PR_PROFILE_HOME_SERVER_FQDN** evita isso.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a2d3c-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2d3c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a2d3c-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a2d3c-120">Protocol specifications</span></span>

<span data-ttu-id="a2d3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2d3c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2d3c-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a2d3c-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a2d3c-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a2d3c-124">Especifica as operações permitidas para os objetos do repositório de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a2d3c-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a2d3c-125">Header files</span></span>

<span data-ttu-id="a2d3c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a2d3c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a2d3c-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a2d3c-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a2d3c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a2d3c-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a2d3c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a2d3c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2d3c-130">See also</span></span>



[<span data-ttu-id="a2d3c-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a2d3c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a2d3c-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a2d3c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a2d3c-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a2d3c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a2d3c-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a2d3c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
