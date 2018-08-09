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
ms.openlocfilehash: ad26cb9b77404d6470f7a8d787eb85edc5cce402
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19766159"
---
# <a name="adrparm"></a><span data-ttu-id="c6fad-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="c6fad-103">ADRPARM</span></span>

<span data-ttu-id="c6fad-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6fad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6fad-105">Descreve a exibição e o comportamento da caixa de diálogo endereço comum.</span><span class="sxs-lookup"><span data-stu-id="c6fad-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6fad-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c6fad-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6fad-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6fad-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c6fad-108">Members</span><span class="sxs-lookup"><span data-stu-id="c6fad-108">Members</span></span>

<span data-ttu-id="c6fad-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="c6fad-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="c6fad-110">Contagem de bytes no identificador de entrada apontado pela **lpABContEntryID**.</span><span class="sxs-lookup"><span data-stu-id="c6fad-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="c6fad-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="c6fad-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="c6fad-112">Ponteiro para o identificador de entrada do contêiner que fornece a lista inicial dos endereços de destinatário que são exibidos na caixa de diálogo endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="c6fad-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c6fad-113">**ulFlags**</span></span>
  
> <span data-ttu-id="c6fad-114">Bitmask dos sinalizadores associados a várias opções de caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="c6fad-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c6fad-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c6fad-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="c6fad-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="c6fad-117">Habilite todos os nomes de ser resolvido depois que a caixa de diálogo de endereço é fechada.</span><span class="sxs-lookup"><span data-stu-id="c6fad-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="c6fad-118">Se houver entradas ambíguas resultantes do processo de resolução de nome, uma caixa de diálogo é exibida avisar o usuário para obter ajuda na resolvê-los.</span><span class="sxs-lookup"><span data-stu-id="c6fad-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="c6fad-119">Configuração esse sinalizador garante que todos os nomes retornados por [IAddrBook::Address](iaddrbook-address.md) forem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="c6fad-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="c6fad-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="c6fad-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="c6fad-121">Desabilite a criação de endereços únicos para uma lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="c6fad-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="c6fad-122">Esse sinalizador é usado somente se a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="c6fad-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="c6fad-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="c6fad-124">O usuário pode selecionar exatamente um destinatário, em vez de vários destinatários de uma lista.</span><span class="sxs-lookup"><span data-stu-id="c6fad-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="c6fad-125">Esse sinalizador é válido somente quando **cDestFields** é zero e a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="c6fad-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="c6fad-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="c6fad-127">Faz com que a versão modal da caixa de diálogo endereço comum a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="c6fad-128">Este sinalizador ou DIALOG_SDI deve ser definido; eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c6fad-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="c6fad-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="c6fad-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="c6fad-130">Faz com que o botão de **Opções de enviar** a ser exibido na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="c6fad-131">Esse sinalizador é usado somente se a caixa de diálogo é modal, conforme indicado pelo sinalizador DIALOG_MODAL sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="c6fad-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="c6fad-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="c6fad-133">Faz com que a versão sem janela restrita da caixa de diálogo endereço comum a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="c6fad-134">Este sinalizador ou DIALOG_MODAL deve ser definido; eles não podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="c6fad-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="c6fad-135">O sinalizador DIALOG_SDI é ignorado para clientes não são do Outlook e a versão modal da caixa de diálogo será exibida.</span><span class="sxs-lookup"><span data-stu-id="c6fad-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="c6fad-136">Consequentemente, um ponteiro para uma alça não deverão ser esperado no parâmetro _lpulUIParam_ do [IAddrBook::Address](iaddrbook-address.md).</span><span class="sxs-lookup"><span data-stu-id="c6fad-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="c6fad-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="c6fad-137">**lpReserved**</span></span>
  
> <span data-ttu-id="c6fad-138">Reservado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c6fad-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="c6fad-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="c6fad-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="c6fad-140">Especifica o contexto dentro de **Ajuda** que será inicialmente exibido quando o usuário clica no botão Ajuda na caixa de diálogo endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="c6fad-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="c6fad-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="c6fad-142">Ponteiro para o nome de um arquivo de Ajuda que será associado a caixa de diálogo de endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="c6fad-143">O membro **lpszHelpFileName** é usado em conjunto com **ulHelpContext** para chamar a função Windows **WinHelp** .</span><span class="sxs-lookup"><span data-stu-id="c6fad-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="c6fad-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="c6fad-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="c6fad-145">Ponteiro para uma função MAPI com base no [ACCELERATEABSDI](accelerateabsdi.md) protótipo ou nulo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="c6fad-146">Este membro se aplica à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="c6fad-147">Clientes criando uma estrutura **ADRPARM** a serem passados para [IAddrBook::Address](iaddrbook-address.md) sempre devem definir o membro **lpfnABSDI** como NULL.</span><span class="sxs-lookup"><span data-stu-id="c6fad-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="c6fad-148">Se o sinalizador DIALOG_SDI estiver definido, MAPI, em seguida, definirá-lo como uma função válida antes de retornar.</span><span class="sxs-lookup"><span data-stu-id="c6fad-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="c6fad-149">Clientes chamar essa função em seu loop de mensagem para certificar-se de que os aceleradores no endereço do livro trabalho da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="c6fad-150">Quando a caixa de diálogo é fechada e MAPI chama a função apontada pelo membro **lpfnDismiss** , os clientes devem solte a função **ACCELERATEABSDI** seu do loop de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c6fad-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="c6fad-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="c6fad-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="c6fad-152">Ponteiro para uma função com base no [DISMISSMODELESS](dismissmodeless.md) protótipo ou nulo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="c6fad-153">Este membro se aplica somente à versão sem janela restrita da caixa de diálogo apenas, conforme indicado pelo sinalizador DIALOG_SDI sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="c6fad-154">MAPI chama a função **DISMISSMODELESS** quando o usuário descarte a caixa de diálogo sem janela restrita endereço informando um cliente chamar **IAddrBook::Address** que a caixa de diálogo não está mais ativa.</span><span class="sxs-lookup"><span data-stu-id="c6fad-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="c6fad-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="c6fad-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="c6fad-156">Ponteiro para informações de contexto a serem passados para a função **DISMISSMODELESS** apontado pelo membro **lpfnDismiss** .</span><span class="sxs-lookup"><span data-stu-id="c6fad-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="c6fad-157">Este membro só se aplica a versão sem janela restrita da caixa de diálogo, conforme indicado pelo sinalizador DIALOG_SDI sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="c6fad-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="c6fad-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="c6fad-159">Ponteiro para o texto a ser usado como o título para a caixa de diálogo endereço comuns.</span><span class="sxs-lookup"><span data-stu-id="c6fad-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="c6fad-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="c6fad-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="c6fad-161">Ponteiro para o texto a ser usado como o rótulo do botão para o botão que invoca a caixa de diálogo **Nova entrada** ou outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="c6fad-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="c6fad-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="c6fad-163">Ponteiro para o texto a ser usado como um título para os controles de caixa de texto de destinatários que podem aparecer na versão modal da caixa de diálogo comum do endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="c6fad-164">Este membro não é usado para caixas de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="c6fad-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="c6fad-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="c6fad-165">**cDestFields**</span></span>
  
> <span data-ttu-id="c6fad-166">Contagem de controles de caixa de texto de destinatário na versão modal de caixa de diálogo endereço ou zero se a caixa de diálogo não é modal.</span><span class="sxs-lookup"><span data-stu-id="c6fad-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="c6fad-167">A caixa de diálogo de endereço está aberta para navegação somente quando as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="c6fad-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="c6fad-168">O membro **cDestFields** é definido como zero.</span><span class="sxs-lookup"><span data-stu-id="c6fad-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="c6fad-169">O sinalizador DIALOG_BOX está definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="c6fad-170">O sinalizador ADDRESS_ONE não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c6fad-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="c6fad-171">A definição de **cDestFields** como 0XFFFFFFFF implica que MAPI deve criar o número padrão de texto destinatário controles da caixa.</span><span class="sxs-lookup"><span data-stu-id="c6fad-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="c6fad-172">Nesse caso, os membros **lppszDestTitles** e **lpulDestComps** devem ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c6fad-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="c6fad-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="c6fad-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="c6fad-174">Indica o controle de caixa de texto específico que deve ter o foco inicial quando a versão modal da caixa de diálogo aparece.</span><span class="sxs-lookup"><span data-stu-id="c6fad-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="c6fad-175">Esse valor deve estar entre 0 e o valor da **cDestFields** menos 1.</span><span class="sxs-lookup"><span data-stu-id="c6fad-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="c6fad-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="c6fad-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="c6fad-177">Ponteiro para uma matriz de rótulos de botões associados a cada um dos controles de caixa de texto que são exibidos na versão da caixa de diálogo endereço modal.</span><span class="sxs-lookup"><span data-stu-id="c6fad-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="c6fad-178">O valor do membro **cDestFields** indica o número de rótulos incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="c6fad-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="c6fad-179">Se o membro **lppszDestTitles** for NULL, o método de **endereços** usa títulos padrão.</span><span class="sxs-lookup"><span data-stu-id="c6fad-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="c6fad-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="c6fad-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="c6fad-181">Ponteiro para uma matriz de valores de tipo de destinatário, como MAPI_TO, MAPI_CC e MAPI_BCC, que é associado a cada controle de caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="c6fad-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="c6fad-182">O valor do membro **CDestFields** indica o número de tipos de destinatários incluídos na matriz.</span><span class="sxs-lookup"><span data-stu-id="c6fad-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="c6fad-183">Os valores apontados pela **lpulDestComps** podem ser usados para definir a propriedade **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="c6fad-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="c6fad-184">Se o membro **lpulDestComps** for NULL, o método de **endereços** usa os tipos de destinatário padrão.</span><span class="sxs-lookup"><span data-stu-id="c6fad-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="c6fad-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="c6fad-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="c6fad-186">Ponteiro para uma estrutura [SRestriction](srestriction.md) que limita o tipo de entradas de endereço que podem ser exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="c6fad-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="c6fad-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="c6fad-188">Ponteiro para uma estrutura **SRestriction** que limita os contêineres do catálogo de endereços que podem fornecer as entradas de endereço a ser exibido na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c6fad-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c6fad-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6fad-189">Remarks</span></span>

<span data-ttu-id="c6fad-190">Estruturas **ADRPARM** são usadas por clientes e provedores de serviços para controlar a aparência e o comportamento das caixas de diálogo de endereço comuns de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c6fad-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="c6fad-191">Existem duas variedades da caixa de diálogo endereço: sem janela restrita e modal.</span><span class="sxs-lookup"><span data-stu-id="c6fad-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="c6fad-192">Alguns dos membros na estrutura **ADRPARM** aplicam às duas versões da caixa de diálogo, mas algumas só se aplicam a uma das duas versões.</span><span class="sxs-lookup"><span data-stu-id="c6fad-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="c6fad-193">A tabela a seguir relaciona os membros de uma estrutura de **ADRPARM** para seu uso com caixas de diálogo comuns do endereço.</span><span class="sxs-lookup"><span data-stu-id="c6fad-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="c6fad-194">Membro ADRPARM</span><span class="sxs-lookup"><span data-stu-id="c6fad-194">ADRPARM member</span></span>|<span data-ttu-id="c6fad-195">Tipo de caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="c6fad-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6fad-196">**cbABContEntryID** e **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="c6fad-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="c6fad-197">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c6fad-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="c6fad-199">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="c6fad-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="c6fad-201">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-202">**ulHelpContext** e **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="c6fad-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="c6fad-203">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="c6fad-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="c6fad-205">Sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-206">**lpfnDismiss** e **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="c6fad-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="c6fad-207">Sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="c6fad-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="c6fad-209">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="c6fad-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="c6fad-211">Modal</span><span class="sxs-lookup"><span data-stu-id="c6fad-211">Modal</span></span>  <br/> |
|<span data-ttu-id="c6fad-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**e **lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="c6fad-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="c6fad-213">Modal</span><span class="sxs-lookup"><span data-stu-id="c6fad-213">Modal</span></span>  <br/> |
|<span data-ttu-id="c6fad-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="c6fad-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="c6fad-215">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="c6fad-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="c6fad-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="c6fad-217">Janela restrita e sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="c6fad-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="c6fad-218">A caixa de diálogo sem janela restrita é uma exibição somente leitura de entradas a partir de um ou mais contêineres do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="c6fad-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="c6fad-219">A caixa de diálogo pode exibir todas as entradas a partir de contêineres selecionados ou ser limitado para apenas aqueles entradas e contêineres que correspondam aos critérios estabelecidos por uma restrição.</span><span class="sxs-lookup"><span data-stu-id="c6fad-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="c6fad-220">A restrição de conteúdo apontada pela **lpContRestriction** pode limitar os tipos de entradas exibidas e a restrição de hierarquia apontada pela **lpHierRestriction** pode limitar os contêineres fornecendo as entradas.</span><span class="sxs-lookup"><span data-stu-id="c6fad-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="c6fad-221">Para informar o chamador quando a caixa de diálogo é fechada, MAPI chama uma função que é fornecida pelo chamador que coincida com o protótipo [DISMISSMODELESS](dismissmodeless.md) .</span><span class="sxs-lookup"><span data-stu-id="c6fad-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="c6fad-222">Outra função, que ele corresponda protótipo [ACCELERATEABSDI](accelerateabsdi.md) , é fornecida pelo MAPI e invocada pelo chamador no loop de mensagem do Windows para facilitar o trabalho de atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="c6fad-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="c6fad-223">A versão sem janela restrita da caixa de diálogo de endereço MAPI pode ser exibida quando clientes chamar [IAddrBook::Address](iaddrbook-address.md) ou quando os provedores de serviço chamarem [IMAPISupport::Address](imapisupport-address.md).</span><span class="sxs-lookup"><span data-stu-id="c6fad-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="c6fad-224">A caixa de diálogo modal é uma exibição de leitura/gravação de entradas a partir de um ou mais contêineres.</span><span class="sxs-lookup"><span data-stu-id="c6fad-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="c6fad-225">Seu conteúdo pode ser afetado da mesma maneira como a versão sem janela restrita por restrições definida no **lpContRestriction** and **lpHierRestriction** membros.</span><span class="sxs-lookup"><span data-stu-id="c6fad-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="c6fad-226">Além da caixa de listagem exibindo entradas do contêiner, a caixa de diálogo modal pode conter entre um e três controles de caixa de texto para reter entradas selecionadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c6fad-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="c6fad-227">Cada controle de edição é associado um determinado tipo de destinatário ou a propriedade **PR_RECIPIENT_TYPE** como MAPI_TO.</span><span class="sxs-lookup"><span data-stu-id="c6fad-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="c6fad-228">A caixa de diálogo modal endereço pode ser exibida por qualquer um dos métodos **endereço** ou quando os clientes chamada [IAddrBook::Details](iaddrbook-details.md) e [IMAPISupport::Details](imapisupport-details.md)de chamada de provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="c6fad-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="c6fad-229">Esta ilustração inclui dois controles de caixa de texto, porque o membro **cDestFields** da estrutura **ADRPARM** controlar a exibição dessa caixa de diálogo é definido como 2.</span><span class="sxs-lookup"><span data-stu-id="c6fad-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="c6fad-230">O primeiro controle tem o foco inicial porque o membro **nDestFieldFocus** está definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c6fad-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="c6fad-231">O membro **lpszNewEntryTitle** aponta para o texto de um rótulo de botão que, quando ele for selecionado, faz com que uma caixa de diálogo adicionais a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="c6fad-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="c6fad-232">Normalmente, conforme mostrado na ilustração da caixa de diálogo modal, o botão está rotulado **New** e a caixa de diálogo que aparece lista todos os tipos de endereços que podem ser criados por qualquer um dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="c6fad-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="c6fad-233">Clientes causam esta caixa de diálogo **Nova entrada** a ser exibido chamando [IAddrBook::NewEntry](iaddrbook-newentry.md) e passando zero para o parâmetro _cbEidNewEntryTpl_ e NULL para o parâmetro _lpEidNewEntryTpl_ quando o usuário seleciona o botão.</span><span class="sxs-lookup"><span data-stu-id="c6fad-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="c6fad-234">As informações que estão incluídas nesta caixa de diálogo proveniente da tabela único de MAPI.</span><span class="sxs-lookup"><span data-stu-id="c6fad-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="c6fad-235">Cada entrada nessa caixa de diálogo é associada um modelo para inserir os dados necessários para criar um endereço do tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="c6fad-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="c6fad-236">A maioria dos provedores de catálogo de endereços fornecer um modelo para cada tipo de entrada de endereço que possam criar.</span><span class="sxs-lookup"><span data-stu-id="c6fad-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="c6fad-237">Quando um usuário faz uma seleção a partir dessa caixa de diálogo, o MAPI exibe o modelo correspondente.</span><span class="sxs-lookup"><span data-stu-id="c6fad-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="c6fad-238">Os quatro bits mais significativos do membro de **ulFlags** da estrutura **ADRPARM** contiverem um número de versão que identifica a versão da estrutura **ADRPARM** .</span><span class="sxs-lookup"><span data-stu-id="c6fad-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="c6fad-239">A versão atual é 0 (zero) ou ADRPARM_HELP_CTX.</span><span class="sxs-lookup"><span data-stu-id="c6fad-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="c6fad-240">A implementação atual do MAPI falhará para qualquer versão da estrutura diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c6fad-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="c6fad-241">Versões futuras da estrutura podem ser completamente diferentes; eles podem não suportar a estrutura de versão de zero.</span><span class="sxs-lookup"><span data-stu-id="c6fad-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="c6fad-242">As seguintes macros são fornecidas para extrair o número da versão do membro **ulFlags** em combinação com os sinalizadores definidos:</span><span class="sxs-lookup"><span data-stu-id="c6fad-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="c6fad-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="c6fad-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="c6fad-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="c6fad-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="c6fad-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="c6fad-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6fad-246">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6fad-246">See also</span></span>

- [<span data-ttu-id="c6fad-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="c6fad-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="c6fad-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="c6fad-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="c6fad-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c6fad-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="c6fad-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="c6fad-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="c6fad-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="c6fad-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="c6fad-252">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6fad-252">MAPI Structures</span></span>](mapi-structures.md)

