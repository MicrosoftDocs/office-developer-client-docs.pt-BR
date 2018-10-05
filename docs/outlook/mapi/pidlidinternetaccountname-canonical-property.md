---
title: Propriedade canônica PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2da826fe7ab9e4d7ca3eaaf0f9806193c47100d1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386674"
---
# <a name="pidlidinternetaccountname-canonical-property"></a><span data-ttu-id="46724-103">Propriedade canônica PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="46724-103">PidLidInternetAccountName Canonical Property</span></span>

  
  
<span data-ttu-id="46724-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46724-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46724-105">Especifica o nome da conta de email do usuário visíveis através do qual a mensagem de email é enviada.</span><span class="sxs-lookup"><span data-stu-id="46724-105">Specifies the user-visible email account name through which the email message is sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46724-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="46724-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46724-107">dispidInetAcctName</span><span class="sxs-lookup"><span data-stu-id="46724-107">dispidInetAcctName</span></span>  <br/> |
|<span data-ttu-id="46724-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="46724-108">Property set:</span></span>  <br/> |<span data-ttu-id="46724-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="46724-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="46724-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="46724-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="46724-111">0x00008580</span><span class="sxs-lookup"><span data-stu-id="46724-111">0x00008580</span></span>  <br/> |
|<span data-ttu-id="46724-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="46724-112">Data type:</span></span>  <br/> |<span data-ttu-id="46724-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46724-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="46724-114">Área:</span><span class="sxs-lookup"><span data-stu-id="46724-114">Area:</span></span>  <br/> |<span data-ttu-id="46724-115">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="46724-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46724-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="46724-116">Remarks</span></span>

<span data-ttu-id="46724-117">O formato dessa cadeia de caracteres é dependente de implementação.</span><span class="sxs-lookup"><span data-stu-id="46724-117">The format of this string is implementation dependent.</span></span> <span data-ttu-id="46724-118">Essa propriedade pode ser usada pelo cliente para determinar em qual servidor para direcionar o email para, mas é opcional e o valor não tem significado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="46724-118">This property can be used by the client to determine which server to direct the mail to, but is optional and the value has no meaning to the server.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46724-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="46724-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46724-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="46724-120">Protocol specifications</span></span>

<span data-ttu-id="46724-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46724-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46724-122">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="46724-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46724-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46724-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46724-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="46724-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46724-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46724-125">Header files</span></span>

<span data-ttu-id="46724-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46724-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="46724-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="46724-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46724-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="46724-128">See also</span></span>



[<span data-ttu-id="46724-129">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="46724-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46724-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="46724-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46724-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="46724-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46724-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="46724-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

