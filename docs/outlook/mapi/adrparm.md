---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330216"
---
# <a name="adrparm"></a><span data-ttu-id="42483-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="42483-103">ADRPARM</span></span>

<span data-ttu-id="42483-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42483-105">Descreve a exibição e o comportamento da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="42483-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42483-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="42483-106">Header file:</span></span>  <br/> |<span data-ttu-id="42483-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="42483-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a><span data-ttu-id="42483-108">Members</span><span class="sxs-lookup"><span data-stu-id="42483-108">Members</span></span>

<span data-ttu-id="42483-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="42483-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="42483-110">Contagem de bytes no identificador de entrada apontado por **lpABContEntryID**.</span><span class="sxs-lookup"><span data-stu-id="42483-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="42483-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="42483-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="42483-112">Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial de endereços de destinatário que são exibidos na caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="42483-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="42483-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="42483-113">**ulFlags**</span></span>
  
> <span data-ttu-id="42483-114">Bitmask de sinalizadores associados a várias opções da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="42483-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="42483-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="42483-115">The following flags can be set:</span></span>
    
<span data-ttu-id="42483-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="42483-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="42483-117">Habilitar todos os nomes a serem resolvidos depois que a caixa de diálogo de endereço for fechada.</span><span class="sxs-lookup"><span data-stu-id="42483-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="42483-118">Se houver entradas ambíguas que resultem do processo de resolução de nomes, uma caixa de diálogo será exibida para solicitar ajuda ao usuário para solucioná-los.</span><span class="sxs-lookup"><span data-stu-id="42483-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="42483-119">A definição desse sinalizador garante que todos os nomes retornados por [IAddrBook:: address](iaddrbook-address.md) sejam resolvidos.</span><span class="sxs-lookup"><span data-stu-id="42483-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="42483-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="42483-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="42483-121">Desabilitar a criação de endereços únicos para uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="42483-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="42483-122">Este sinalizador é usado apenas se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="42483-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="42483-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="42483-124">O usuário pode selecionar exatamente um destinatário em vez de vários destinatários de uma lista.</span><span class="sxs-lookup"><span data-stu-id="42483-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="42483-125">Este sinalizador é válido somente quando o **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="42483-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="42483-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="42483-127">Faz com que a versão modal da caixa de diálogo de endereço comum seja exibida.</span><span class="sxs-lookup"><span data-stu-id="42483-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="42483-128">Este sinalizador ou DIALOG_SDI deve ser definido; Eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="42483-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="42483-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="42483-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="42483-130">Faz com que o botão **Opções de envio** seja exibido na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42483-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="42483-131">Este sinalizador é usado apenas se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="42483-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="42483-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="42483-133">Faz com que a versão sem janela restrita da caixa de diálogo de endereço comum seja exibida.</span><span class="sxs-lookup"><span data-stu-id="42483-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="42483-134">Este sinalizador ou DIALOG_MODAL deve ser definido; Eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="42483-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="42483-135">O sinalizador DIALOG_SDI é ignorado para clientes que não são do Outlook e a versão modal da caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="42483-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="42483-136">Consequentemente, um ponteiro para um identificador não deve ser esperado no parâmetro _lpulUIParam_ de [IAddrBook:: address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="42483-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="42483-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="42483-137">**lpReserved**</span></span>
  
> <span data-ttu-id="42483-138">Reservado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="42483-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="42483-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="42483-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="42483-140">Especifica o contexto dentro da **ajuda** que será mostrado primeiro quando o usuário clicar no botão ajuda na caixa de diálogo endereço.</span><span class="sxs-lookup"><span data-stu-id="42483-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="42483-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="42483-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="42483-142">Ponteiro para o nome de um arquivo de ajuda que será associado à caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="42483-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="42483-143">O membro **lpszHelpFileName** é usado em conjunto com o **ulHelpContext** para chamar a função **WinHelp** do Windows.</span><span class="sxs-lookup"><span data-stu-id="42483-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="42483-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="42483-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="42483-145">Ponteiro para uma função MAPI com base no protótipo [ACCELERATEABSDI](accelerateabsdi.md) ou nulo.</span><span class="sxs-lookup"><span data-stu-id="42483-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="42483-146">Este membro se aplica à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="42483-147">Os clientes que criam uma estrutura **ADRPARM** para passar para o [IAddrBook:: o endereço](iaddrbook-address.md) deve sempre definir o membro **lpfnABSDI** como nulo.</span><span class="sxs-lookup"><span data-stu-id="42483-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="42483-148">Se o sinalizador DIALOG_SDI estiver definido, o MAPI irá defini-lo como uma função válida antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="42483-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="42483-149">Os clientes chamam essa função no loop de mensagens para garantir que os aceleradores da caixa de diálogo do catálogo de endereços funcionem.</span><span class="sxs-lookup"><span data-stu-id="42483-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="42483-150">Quando a caixa de diálogo é ignorada e MAPI chama a função indicada pelo membro **lpfnDismiss** , os clientes devem desenganchar a função **ACCELERATEABSDI** de seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="42483-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="42483-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="42483-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="42483-152">Ponteiro para uma função com base no protótipo [DISMISSMODELESS](dismissmodeless.md) ou nulo.</span><span class="sxs-lookup"><span data-stu-id="42483-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="42483-153">Este membro só se aplica à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="42483-154">MAPI chama a função **DISMISSMODELESS** quando o usuário ignora a caixa de diálogo de endereço sem restrições, informando um cliente chamando **IAddrBook:: address** que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="42483-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="42483-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="42483-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="42483-156">Ponteiro para informações de contexto a serem passadas para a função **DISMISSMODELESS** indicada pelo membro **lpfnDismiss** .</span><span class="sxs-lookup"><span data-stu-id="42483-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="42483-157">Este membro se aplica apenas à versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="42483-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="42483-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="42483-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="42483-159">Ponteiro para o texto a ser usado como o título da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="42483-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="42483-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="42483-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="42483-161">Ponteiro para o texto a ser usado como o rótulo do botão que invoca a caixa de diálogo **nova entrada** ou outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42483-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="42483-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="42483-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="42483-163">Ponteiro para o texto a ser usado como um título para os controles de caixa de texto do destinatário que podem aparecer na versão modal da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="42483-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="42483-164">Este membro não é usado para caixas de diálogo sem restrições.</span><span class="sxs-lookup"><span data-stu-id="42483-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="42483-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="42483-165">**cDestFields**</span></span>
  
> <span data-ttu-id="42483-166">Contagem de controles de caixa de texto do destinatário na versão modal da caixa de diálogo endereço ou zero se a caixa de diálogo for sem restrições.</span><span class="sxs-lookup"><span data-stu-id="42483-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="42483-167">A caixa de diálogo endereço é aberta para navegação somente quando as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="42483-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="42483-168">O membro **cDestFields** está definido como zero.</span><span class="sxs-lookup"><span data-stu-id="42483-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="42483-169">O sinalizador DIALOG_BOX está definido.</span><span class="sxs-lookup"><span data-stu-id="42483-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="42483-170">O sinalizador ADDRESS_ONE não está definido.</span><span class="sxs-lookup"><span data-stu-id="42483-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="42483-171">A definição de **cDestFields** como 0xFFFFFFFF implica que o MAPI deve criar o número padrão de controles de caixa de texto do destinatário.</span><span class="sxs-lookup"><span data-stu-id="42483-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="42483-172">Nesse caso, os membros **lppszDestTitles** e **LPULDESTCOMPS** devem ser nulos.</span><span class="sxs-lookup"><span data-stu-id="42483-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="42483-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="42483-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="42483-174">Indica o controle de caixa de texto específico que deverá ter o foco inicial quando a versão modal da caixa de diálogo for exibida.</span><span class="sxs-lookup"><span data-stu-id="42483-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="42483-175">Esse valor deve estar entre 0 e o valor de **cDestFields** menos 1.</span><span class="sxs-lookup"><span data-stu-id="42483-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="42483-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="42483-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="42483-177">Ponteiro para uma matriz de rótulos de botões associados a cada um dos controles de caixa de texto que são exibidos na versão modal da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="42483-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="42483-178">O valor do membro **cDestFields** indica o número de rótulos incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="42483-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="42483-179">Se o membro **lppszDestTitles** for nulo, o método **Address** usará títulos padrão.</span><span class="sxs-lookup"><span data-stu-id="42483-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="42483-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="42483-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="42483-181">Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que é associado a cada controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="42483-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="42483-182">O valor do membro **CDestFields** indica o número de tipos de destinatários incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="42483-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="42483-183">Os valores apontados por **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="42483-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="42483-184">Se o membro **lpulDestComps** for nulo, o método **Address** usará tipos de destinatário padrão.</span><span class="sxs-lookup"><span data-stu-id="42483-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="42483-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="42483-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="42483-186">Ponteiro para uma estrutura [SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidas na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42483-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="42483-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="42483-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="42483-188">Ponteiro para uma estrutura **SRestriction** que limita os contêineres do catálogo de endereços que podem fornecer entradas de endereço a serem exibidas na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42483-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42483-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="42483-189">Remarks</span></span>

<span data-ttu-id="42483-190">As estruturas **ADRPARM** são usadas por clientes e provedores de serviço para controlar a aparência e o comportamento das caixas de diálogo de endereço comum MAPI.</span><span class="sxs-lookup"><span data-stu-id="42483-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="42483-191">Há duas variedades da caixa de diálogo de endereço: sem-modo e modal.</span><span class="sxs-lookup"><span data-stu-id="42483-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="42483-192">Alguns membros da estrutura **ADRPARM** aplicam-se às duas versões da caixa de diálogo, mas algumas só se aplicam a uma das duas versões.</span><span class="sxs-lookup"><span data-stu-id="42483-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="42483-193">A tabela a seguir relaciona os membros de uma estrutura **ADRPARM** ao uso com as caixas de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="42483-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="42483-194">Membro ADRPARM</span><span class="sxs-lookup"><span data-stu-id="42483-194">ADRPARM member</span></span>|<span data-ttu-id="42483-195">Tipo de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="42483-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="42483-196">**cbABContEntryID** e **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="42483-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="42483-197">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="42483-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="42483-199">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="42483-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="42483-201">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-202">**ulHelpContext** e **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="42483-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="42483-203">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="42483-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="42483-205">Sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="42483-206">**lpfnDismiss** e **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="42483-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="42483-207">Sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="42483-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="42483-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="42483-209">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="42483-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="42483-211">Modal</span><span class="sxs-lookup"><span data-stu-id="42483-211">Modal</span></span>  <br/> |
|<span data-ttu-id="42483-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**e **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="42483-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="42483-213">Modal</span><span class="sxs-lookup"><span data-stu-id="42483-213">Modal</span></span>  <br/> |
|<span data-ttu-id="42483-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="42483-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="42483-215">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="42483-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="42483-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="42483-217">Modal e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="42483-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="42483-218">A caixa de diálogo sem-modo é uma exibição somente leitura das entradas de um ou mais contêineres do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="42483-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="42483-219">A caixa de diálogo pode exibir todas as entradas dos contêineres selecionados ou ser limitada apenas às entradas e aos contêineres que correspondam aos critérios estabelecidos por uma restrição.</span><span class="sxs-lookup"><span data-stu-id="42483-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="42483-220">A restrição de conteúdo indicada por **lpContRestriction** pode limitar os tipos de entradas exibidas e a restrição de hierarquia indicada por **lpHierRestriction** pode limitar os contêineres que fornecem as entradas.</span><span class="sxs-lookup"><span data-stu-id="42483-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="42483-221">Para informar o chamador quando a caixa de diálogo é ignorada, o MAPI invoca uma função que é fornecida pelo chamador que corresponde ao protótipo [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="42483-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="42483-222">Outra função, que corresponde ao protótipo [ACCELERATEABSDI](accelerateabsdi.md) , é fornecida por MAPI e invocada pelo chamador no loop de mensagem do Windows para facilitar o trabalho de atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="42483-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="42483-223">A versão sem restrições da caixa de diálogo de endereço MAPI pode ser exibida quando os clientes chamam [IAddrBook:: address](iaddrbook-address.md) ou quando os provedores de serviço chamam [IMAPISupport:: address](imapisupport-address.md).</span><span class="sxs-lookup"><span data-stu-id="42483-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="42483-224">A caixa de diálogo modal é uma exibição de leitura/gravação de entradas de um ou mais contêineres.</span><span class="sxs-lookup"><span data-stu-id="42483-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="42483-225">Seu conteúdo pode ser afetado da mesma maneira que a versão sem janela restrita por restrições definidas nos membros **lpContRestriction** e **lpHierRestriction** .</span><span class="sxs-lookup"><span data-stu-id="42483-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="42483-226">Além da caixa de listagem exibindo entradas de contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para conter entradas selecionadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="42483-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="42483-227">Cada controle de edição é associado a um tipo de destinatário específico ou a propriedade **PR_RECIPIENT_TYPE** , como MAPI_TO.</span><span class="sxs-lookup"><span data-stu-id="42483-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="42483-228">A caixa de diálogo Endereço modal pode ser exibida por qualquer um dos métodos **Address** ou quando os clientes chamam [IAddrBook::D etails](iaddrbook-details.md) e provedores de serviço chamam [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="42483-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="42483-229">Esta ilustração inclui dois controles de caixa de texto porque o membro **cDestFields** da estrutura **ADRPARM** que controla a exibição dessa caixa de diálogo é definido como 2.</span><span class="sxs-lookup"><span data-stu-id="42483-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="42483-230">O primeiro controle tem o foco inicial porque o membro **nDestFieldFocus** está definido como 0.</span><span class="sxs-lookup"><span data-stu-id="42483-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="42483-231">O membro **lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando é selecionado, faz com que uma caixa de diálogo adicional seja exibida.</span><span class="sxs-lookup"><span data-stu-id="42483-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="42483-232">Normalmente, como é mostrado na ilustração da caixa de diálogo modal, o botão é rotulado como **novo** e a caixa de diálogo exibida lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="42483-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="42483-233">Os clientes fazem com que essa nova caixa de diálogo de **entrada** seja exibida chamando [IAddrBook:: NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e nulo para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão.</span><span class="sxs-lookup"><span data-stu-id="42483-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="42483-234">As informações incluídas nessa caixa de diálogo vêm da tabela de one-off MAPI.</span><span class="sxs-lookup"><span data-stu-id="42483-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="42483-235">Cada entrada nessa caixa de diálogo é associada a um modelo para inserir os dados necessários para criar um endereço do tipo específico.</span><span class="sxs-lookup"><span data-stu-id="42483-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="42483-236">A maioria dos provedores de catálogos de endereços fornecem um modelo para cada tipo de entrada de endereço que eles podem criar.</span><span class="sxs-lookup"><span data-stu-id="42483-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="42483-237">Quando um usuário faz uma seleção nessa caixa de diálogo, MAPI exibe o modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="42483-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="42483-238">Os quatro bits mais significativos do membro **parâmetroulflags** da estrutura **ADRPARM** contêm um número de versão que identifica a versão da estrutura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="42483-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="42483-239">A versão atual é 0 (zero) ou ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="42483-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="42483-240">A implementação atual de MAPI irá falhar para qualquer versão da estrutura diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="42483-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="42483-241">Versões futuras da estrutura podem ser completamente diferentes; Eles podem não oferecer suporte à estrutura de versão zero.</span><span class="sxs-lookup"><span data-stu-id="42483-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="42483-242">As macros a seguir são fornecidas para extrair o número de versão do membro **parâmetroulflags** e para combiná-lo com os sinalizadores definidos:</span><span class="sxs-lookup"><span data-stu-id="42483-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="42483-243">**GET_ADRPARM_VERSION** (_parâmetroulflags_)</span><span class="sxs-lookup"><span data-stu-id="42483-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="42483-244">**SET_ADRPARM_VERSION** (_parâmetroulflags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="42483-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="42483-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="42483-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42483-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="42483-246">See also</span></span>

- [<span data-ttu-id="42483-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="42483-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="42483-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="42483-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="42483-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="42483-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="42483-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="42483-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="42483-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="42483-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="42483-252">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="42483-252">MAPI Structures</span></span>](mapi-structures.md)

