---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtém uma cadeia de caracteres que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404334"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="85c16-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="85c16-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="85c16-104">Obtém uma cadeia de caracteres que representa uma coleção de atividades de cada um dos usuários especificados pelo _parâmetro hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="85c16-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="85c16-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85c16-105">Parameters</span></span>

<span data-ttu-id="85c16-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="85c16-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="85c16-107">[in] Uma estrutura que especifica uma matriz de endereços SMTP com hashed para um conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="85c16-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="85c16-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="85c16-108">_startTime_</span></span>
  
> <span data-ttu-id="85c16-109">[in] O tempo após o qual as atividades criadas seriam retornadas.</span><span class="sxs-lookup"><span data-stu-id="85c16-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="85c16-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="85c16-110">_activities_</span></span>
  
> <span data-ttu-id="85c16-111">[out] Uma cadeia de caracteres XML que representa o conjunto de atividades dos usuários especificados por _hashedAddresses_ na rede social desde _o início._</span><span class="sxs-lookup"><span data-stu-id="85c16-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85c16-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="85c16-112">Remarks</span></span>

<span data-ttu-id="85c16-113">O OSC **chamará GetActivitiesEx** se o provedor OSC suportar a sincronização sob demanda de atividades.</span><span class="sxs-lookup"><span data-stu-id="85c16-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="85c16-114">O OSC armazena as informações retornadas em  _atividades_ na memória.</span><span class="sxs-lookup"><span data-stu-id="85c16-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="85c16-115">Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="85c16-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="85c16-116">A partir do Outlook Social Connector 2013, o OSC suporta apenas a sincronização sob demanda de atividades e chama **somente GetActivitiesEx** para obter atividades.</span><span class="sxs-lookup"><span data-stu-id="85c16-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="85c16-117">Para dar suporte à pesquisa de atividades sob demanda, de definir **cacheActivities** como **falso** e **getActivities** e **dynamicActivitiesLookupEx** como **verdadeiro,** e o OSC chamará **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="85c16-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="85c16-118">A cadeia de caracteres XML retornada deve estar em conformidade com a definição de esquema para **activityFeed**, conforme definido no esquema para extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="85c16-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="85c16-119">O  _sring hashedAddresses_ representa um conjunto de endereços com hashed para cada usuário exibido no Painel de Pessoas.</span><span class="sxs-lookup"><span data-stu-id="85c16-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="85c16-120">Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos do** provedor.</span><span class="sxs-lookup"><span data-stu-id="85c16-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="85c16-121">O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="85c16-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="85c16-122">O  _parâmetro startTime_ é um **valor Date** no Tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="85c16-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="85c16-123">Os valores de hora local devem ser convertidos em valores **de Data** UTC.</span><span class="sxs-lookup"><span data-stu-id="85c16-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="85c16-124">As atividades que **o método GetActivitiesEx** retorna devem ter um valor de hora de criação maior que  _startTime_ e menor ou igual a **Now**.</span><span class="sxs-lookup"><span data-stu-id="85c16-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="85c16-125">Se nenhuma alteração tiver ocorrido entre **startTime** e **Now**, o provedor deverá retornar um OSC_E_NO_CHANGES erro.</span><span class="sxs-lookup"><span data-stu-id="85c16-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="85c16-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c16-126">See also</span></span>

- [<span data-ttu-id="85c16-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85c16-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="85c16-128">Sincronizar amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="85c16-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

