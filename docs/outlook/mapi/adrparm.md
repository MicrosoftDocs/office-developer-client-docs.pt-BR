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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425894"
---
# <a name="adrparm"></a><span data-ttu-id="0c797-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="0c797-103">ADRPARM</span></span>

<span data-ttu-id="0c797-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c797-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c797-105">Descreve a exibição e o comportamento da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="0c797-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c797-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0c797-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c797-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c797-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="0c797-108">Members</span><span class="sxs-lookup"><span data-stu-id="0c797-108">Members</span></span>

<span data-ttu-id="0c797-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="0c797-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="0c797-110">Contagem de bytes no identificador de entrada apontado por **lpABContEntryID**.</span><span class="sxs-lookup"><span data-stu-id="0c797-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="0c797-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="0c797-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="0c797-112">Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial de endereços de destinatários que são exibidos na caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="0c797-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="0c797-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="0c797-113">**ulFlags**</span></span>
  
> <span data-ttu-id="0c797-114">Máscara de bits de sinalizadores associados a várias opções de caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="0c797-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="0c797-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0c797-115">The following flags can be set:</span></span>
    
<span data-ttu-id="0c797-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="0c797-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="0c797-117">Habilita todos os nomes a serem resolvidos depois que a caixa de diálogo de endereço é fechada.</span><span class="sxs-lookup"><span data-stu-id="0c797-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="0c797-118">Se houver entradas ambíguas resultantes do processo de resolução de nomes, uma caixa de diálogo aparecerá solicitando ao usuário ajuda para resolvê-las.</span><span class="sxs-lookup"><span data-stu-id="0c797-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="0c797-119">Definir esse sinalizador garante que todos os nomes retornados por [IAddrBook::Address](iaddrbook-address.md) sejam resolvidos.</span><span class="sxs-lookup"><span data-stu-id="0c797-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="0c797-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="0c797-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="0c797-121">Desabilite a criação de endereços one-off para uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="0c797-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="0c797-122">Esse sinalizador é usado somente se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="0c797-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="0c797-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="0c797-124">O usuário pode selecionar exatamente um destinatário em vez de vários destinatários de uma lista.</span><span class="sxs-lookup"><span data-stu-id="0c797-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="0c797-125">Esse sinalizador só é válido quando **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="0c797-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="0c797-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="0c797-127">Faz com que a versão modal da caixa de diálogo de endereço comum seja exibida.</span><span class="sxs-lookup"><span data-stu-id="0c797-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="0c797-128">Esse sinalizador ou DIALOG_SDI deve ser definido; eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="0c797-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="0c797-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="0c797-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="0c797-130">Faz com **que o** botão Opções de Envio seja exibido na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0c797-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="0c797-131">Esse sinalizador é usado somente se a caixa de diálogo for modal, conforme indicado pelo sinalizador DIALOG_MODAL está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="0c797-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="0c797-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="0c797-133">Faz com que a versão sem modo da caixa de diálogo de endereço comum seja exibida.</span><span class="sxs-lookup"><span data-stu-id="0c797-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="0c797-134">Esse sinalizador ou DIALOG_MODAL deve ser definido; eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="0c797-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="0c797-135">O DIALOG_SDI sinalizador é ignorado para clientes que não são do Outlook e a versão modal da caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="0c797-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="0c797-136">Consequentemente, um ponteiro para um indicador não deve ser esperado no parâmetro  _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="0c797-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="0c797-137">**lpReserved**</span></span>
  
> <span data-ttu-id="0c797-138">Reservado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c797-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="0c797-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="0c797-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="0c797-140">Especifica o contexto na **Ajuda** que será exibido primeiro quando o usuário clicar no botão Ajuda na caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="0c797-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="0c797-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="0c797-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="0c797-142">Ponteiro para o nome de um arquivo de Ajuda que será associado à caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="0c797-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="0c797-143">O **membro lpszHelpFileName** é usado junto com **ulHelpContext** para chamar a função **WinHelp do** Windows.</span><span class="sxs-lookup"><span data-stu-id="0c797-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="0c797-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="0c797-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="0c797-145">Ponteiro para uma função MAPI com base no protótipo [ACCELERATEABSDI](accelerateabsdi.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="0c797-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="0c797-146">Esse membro se aplica somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="0c797-147">Os clientes que estão criando uma estrutura **ADRPARM** para passar para [IAddrBook::Address](iaddrbook-address.md) devem sempre definir o membro **lpfnABSDI** como NULL.</span><span class="sxs-lookup"><span data-stu-id="0c797-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="0c797-148">Se o DIALOG_SDI sinalizador estiver definido, o MAPI o definirá como uma função válida antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="0c797-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="0c797-149">Os clientes chamam essa função no loop de mensagens para garantir que os aceleradores na caixa de diálogo do livro de endereços funcionem.</span><span class="sxs-lookup"><span data-stu-id="0c797-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="0c797-150">Quando a caixa de diálogo é descartada e MAPI chama a função apontada pelo membro **lpfnDismiss,** os clientes devem desaconsinchar a função **ACCELERATEABSDI** de seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0c797-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="0c797-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="0c797-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="0c797-152">Ponteiro para uma função baseada no protótipo [DISMISSMODELESS](dismissmodeless.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="0c797-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="0c797-153">Esse membro só se aplica à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="0c797-154">MAPI calls the **DISMISSMODELESS function** when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span><span class="sxs-lookup"><span data-stu-id="0c797-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="0c797-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="0c797-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="0c797-156">Ponteiro para informações de contexto a serem passadas para a **função DISMISSMODELESS** apontada pelo **membro lpfnDismiss.**</span><span class="sxs-lookup"><span data-stu-id="0c797-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="0c797-157">Este membro aplica-se somente à versão sem modo da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="0c797-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="0c797-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="0c797-159">Ponteiro para texto a ser usado como o título da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="0c797-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="0c797-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="0c797-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="0c797-161">Ponteiro para texto a ser usado como o rótulo  do botão para o botão que invoca a caixa de diálogo Nova Entrada ou outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0c797-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="0c797-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="0c797-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="0c797-163">Ponteiro para texto a ser usado como um título para os controles de caixa de texto do destinatário que podem aparecer na versão modal da caixa de diálogo de endereço comum.</span><span class="sxs-lookup"><span data-stu-id="0c797-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="0c797-164">Este membro não é usado para caixas de diálogo sem modo.</span><span class="sxs-lookup"><span data-stu-id="0c797-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="0c797-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="0c797-165">**cDestFields**</span></span>
  
> <span data-ttu-id="0c797-166">Contagem de controles de caixa de texto do destinatário na versão modal da caixa de diálogo de endereço ou zero se a caixa de diálogo não tiver nenhuma.</span><span class="sxs-lookup"><span data-stu-id="0c797-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="0c797-167">A caixa de diálogo de endereço está aberta para navegação somente quando as seguintes condições são verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="0c797-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="0c797-168">O **membro cDestFields** é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="0c797-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="0c797-169">O DIALOG_BOX sinalizador está definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="0c797-170">O ADDRESS_ONE sinalizador não está definido.</span><span class="sxs-lookup"><span data-stu-id="0c797-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="0c797-171">Definir **cDestFields** como 0XFFFFFFFF indica que MAPI deve criar o número padrão de controles de caixa de texto do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c797-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="0c797-172">Nesse caso, os **membros lppszDestTitles** e **lpulDestComps** devem ser NULL.</span><span class="sxs-lookup"><span data-stu-id="0c797-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="0c797-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="0c797-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="0c797-174">Indica o controle de caixa de texto específico que deve ter o foco inicial quando a versão modal da caixa de diálogo for exibida.</span><span class="sxs-lookup"><span data-stu-id="0c797-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="0c797-175">Esse valor deve estar entre 0 e o valor de **cDestFields** menos 1.</span><span class="sxs-lookup"><span data-stu-id="0c797-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="0c797-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="0c797-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="0c797-177">Ponteiro para uma matriz de rótulos para botões associados a cada um dos controles de caixa de texto que são exibidos na versão modal da caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="0c797-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="0c797-178">O valor do **membro cDestFields** indica o número de rótulos incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="0c797-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="0c797-179">Se o **membro lppszDestTitles** for NULL, o método **Address** usará títulos padrão.</span><span class="sxs-lookup"><span data-stu-id="0c797-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="0c797-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="0c797-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="0c797-181">Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que está associada a cada controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="0c797-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="0c797-182">O valor do **membro CDestFields** indica o número de tipos de destinatários incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="0c797-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="0c797-183">Os valores apontados por **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="0c797-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="0c797-184">Se o **membro lpulDestComps** for NULL, o método **Address** usará tipos de destinatário padrão.</span><span class="sxs-lookup"><span data-stu-id="0c797-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="0c797-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="0c797-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="0c797-186">Ponteiro para uma [estrutura SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidas na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0c797-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="0c797-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="0c797-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="0c797-188">Ponteiro para uma **estrutura SRestriction** que limita os contêineres do livro de endereços que podem fornecer entradas de endereço a serem exibidas na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0c797-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0c797-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c797-189">Remarks</span></span>

<span data-ttu-id="0c797-190">**As estruturas ADRPARM** são usadas por clientes e provedores de serviços para controlar a aparência e o comportamento das caixas de diálogo de endereço comuns MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c797-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="0c797-191">Há duas variedades de caixa de diálogo de endereço: sem modo e modal.</span><span class="sxs-lookup"><span data-stu-id="0c797-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="0c797-192">Alguns dos membros na estrutura **ADRPARM** se aplicam às duas versões da caixa de diálogo, mas alguns se aplicam apenas a uma das duas versões.</span><span class="sxs-lookup"><span data-stu-id="0c797-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="0c797-193">A tabela a seguir relaciona os membros de uma estrutura **ADRPARM** ao seu uso com as caixas de diálogo de endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="0c797-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="0c797-194">Membro ADRPARM</span><span class="sxs-lookup"><span data-stu-id="0c797-194">ADRPARM member</span></span>|<span data-ttu-id="0c797-195">Tipo de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="0c797-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="0c797-196">**cbABContEntryID** e **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="0c797-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="0c797-197">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="0c797-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="0c797-199">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="0c797-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="0c797-201">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-202">**ulHelpContext** e **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="0c797-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="0c797-203">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="0c797-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="0c797-205">Sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-206">**lpfnDismiss** e **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="0c797-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="0c797-207">Sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="0c797-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="0c797-209">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="0c797-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="0c797-211">Modal</span><span class="sxs-lookup"><span data-stu-id="0c797-211">Modal</span></span>  <br/> |
|<span data-ttu-id="0c797-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** e **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="0c797-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="0c797-213">Modal</span><span class="sxs-lookup"><span data-stu-id="0c797-213">Modal</span></span>  <br/> |
|<span data-ttu-id="0c797-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="0c797-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="0c797-215">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="0c797-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="0c797-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="0c797-217">Modal e sem modo</span><span class="sxs-lookup"><span data-stu-id="0c797-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="0c797-218">A caixa de diálogo sem modo é uma exibição somente leitura de entradas de um ou mais contêineres de livro de endereços.</span><span class="sxs-lookup"><span data-stu-id="0c797-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="0c797-219">A caixa de diálogo pode exibir todas as entradas dos contêineres selecionados ou ser limitada apenas às entradas e contêineres que corresponderem aos critérios estabelecidos por uma restrição.</span><span class="sxs-lookup"><span data-stu-id="0c797-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="0c797-220">A restrição de conteúdo apontada por **lpContRestriction** pode limitar os tipos de entradas exibidas, e a restrição de hierarquia apontada por **lpHierRestriction** pode limitar os contêineres que fornecerem as entradas.</span><span class="sxs-lookup"><span data-stu-id="0c797-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="0c797-221">Para informar ao chamador quando a caixa de diálogo é descartada, o MAPI invoca uma função fornecida pelo chamador que corresponde ao protótipo [DISMISSMODELESS.](dismissmodeless.md)</span><span class="sxs-lookup"><span data-stu-id="0c797-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="0c797-222">Outra função, que corresponde ao protótipo [ACCELERATEABSDI,](accelerateabsdi.md) é fornecida por MAPI e invocada pelo chamador no loop de mensagens do Windows para facilitar o trabalho de atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="0c797-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="0c797-223">A versão sem modo da caixa de diálogo endereço MAPI pode ser exibida quando os clientes chamam [IAddrBook::Address](iaddrbook-address.md) ou quando os provedores de serviços chamam [IMAPISupport::Address](imapisupport-address.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="0c797-224">A caixa de diálogo modal é uma exibição de leitura/gravação de entradas de um ou mais contêineres.</span><span class="sxs-lookup"><span data-stu-id="0c797-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="0c797-225">Seu conteúdo pode ser afetado da mesma maneira que a versão sem restrições definida nos membros **lpContRestriction** e **lpHierRestriction.**</span><span class="sxs-lookup"><span data-stu-id="0c797-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="0c797-226">Além da caixa de listagem exibindo entradas de contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para manter entradas selecionadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0c797-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="0c797-227">Cada controle de edição é associado a um determinado tipo de destinatário **ou** PR_RECIPIENT_TYPE propriedade, como MAPI_TO.</span><span class="sxs-lookup"><span data-stu-id="0c797-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="0c797-228">A caixa de diálogo endereço modal pode ser exibida por qualquer um dos métodos **address** ou quando os clientes chamam [IAddrBook::D etails](iaddrbook-details.md) and service providers call [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="0c797-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="0c797-229">Esta ilustração inclui dois controles de caixa de texto porque o membro **cDestFields** da estrutura **ADRPARM** que controla a exibição dessa caixa de diálogo é definido como 2.</span><span class="sxs-lookup"><span data-stu-id="0c797-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="0c797-230">O primeiro controle tem foco inicial porque o **membro nDestFieldFocus** está definido como 0.</span><span class="sxs-lookup"><span data-stu-id="0c797-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="0c797-231">O **membro lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando selecionado, faz com que uma caixa de diálogo adicional seja exibida.</span><span class="sxs-lookup"><span data-stu-id="0c797-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="0c797-232">Normalmente, como é mostrado na ilustração da caixa de diálogo  modal, o botão é rotulado como Novo e a caixa de diálogo que aparece lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de agenda do perfil.</span><span class="sxs-lookup"><span data-stu-id="0c797-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="0c797-233">Os clientes  podem exibir essa caixa de diálogo Nova Entrada chamando [IAddrBook::NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e NULL para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão.</span><span class="sxs-lookup"><span data-stu-id="0c797-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="0c797-234">As informações incluídas nesta caixa de diálogo vêm da tabela única MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c797-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="0c797-235">Cada entrada nessa caixa de diálogo é associada a um modelo para inserir os dados necessários para criar um endereço do tipo específico.</span><span class="sxs-lookup"><span data-stu-id="0c797-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="0c797-236">A maioria dos provedores de livro de endereços fornece um modelo para cada tipo de entrada de endereço que eles podem criar.</span><span class="sxs-lookup"><span data-stu-id="0c797-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="0c797-237">Quando um usuário faz uma seleção a partir dessa caixa de diálogo, MAPI exibe o modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="0c797-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="0c797-238">Os quatro bits mais significativos do membro **ulFlags** da estrutura **ADRPARM** contêm um número de versão que identifica a versão da estrutura **ADRPARM.**</span><span class="sxs-lookup"><span data-stu-id="0c797-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="0c797-239">A versão atual é 0 (zero) ou ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="0c797-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="0c797-240">A implementação atual do MAPI falhará para qualquer versão da estrutura diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0c797-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="0c797-241">Versões futuras da estrutura podem ser completamente diferentes; eles podem não dar suporte à estrutura de versão zero.</span><span class="sxs-lookup"><span data-stu-id="0c797-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="0c797-242">As macros a seguir são fornecidas para extrair o número de versão do membro **ulFlags** e combiná-lo com os sinalizadores definidos:</span><span class="sxs-lookup"><span data-stu-id="0c797-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="0c797-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="0c797-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="0c797-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="0c797-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="0c797-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="0c797-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c797-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c797-246">See also</span></span>

- [<span data-ttu-id="0c797-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="0c797-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="0c797-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="0c797-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="0c797-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="0c797-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="0c797-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="0c797-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="0c797-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="0c797-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="0c797-252">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="0c797-252">MAPI Structures</span></span>](mapi-structures.md)

