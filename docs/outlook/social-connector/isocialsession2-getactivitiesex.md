---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtém um string que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770867"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="8e9fc-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="8e9fc-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="8e9fc-104">Obtém um string que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="8e9fc-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="8e9fc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e9fc-105">Parameters</span></span>

<span data-ttu-id="8e9fc-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="8e9fc-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="8e9fc-107">[in] Uma estrutura que especifica uma matriz de SMTP com hash endereços para um conjunto de usuários.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="8e9fc-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="8e9fc-108">_startTime_</span></span>
  
> <span data-ttu-id="8e9fc-109">[in] O tempo após o qual as atividades que são criadas serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="8e9fc-110">_atividades_</span><span class="sxs-lookup"><span data-stu-id="8e9fc-110">_activities_</span></span>
  
> <span data-ttu-id="8e9fc-111">[out] Uma sequência de caracteres XML que representa o conjunto de atividades dos usuários especificados pelo _hashedAddresses_ na rede social desde _startTime_.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e9fc-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e9fc-112">Remarks</span></span>

<span data-ttu-id="8e9fc-113">O OSC chama **GetActivitiesEx** se o provedor do OSC oferece suporte a sincronização sob demanda de atividades.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="8e9fc-114">O OSC armazena as informações retornadas em _atividades_ na memória.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="8e9fc-115">Para obter mais informações sobre como o OSC usa e atualiza a essas informações na memória, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="8e9fc-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="8e9fc-116">Iniciando no Outlook Social Connector 2013, o OSC suporta apenas sob demanda sincronização de atividades e chama apenas **GetActivitiesEx** para fazer atividades.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="8e9fc-117">Para dar suporte à pesquisa de atividades sob demanda, defina **cacheActivities** como **Falso**e **getActivities** e **dynamicActivitiesLookupEx** como **true**e o OSC chamará **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="8e9fc-118">A cadeia de caracteres XML retornada deve estar em conformidade com a definição de esquema do **feed de atividades**, conforme definido no esquema para extensibilidade do provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="8e9fc-119">O sring _hashedAddresses_ representa um conjunto de endereços de hash para cada usuário exibida no painel de pessoas.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="8e9fc-120">Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** nos do provedor **capacidades** de XML.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="8e9fc-121">O usuário não precisa ser um amigo do logon de usuário representado pela propriedade [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="8e9fc-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="8e9fc-122">O parâmetro _startTime_ é um valor de **Data** no tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="8e9fc-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8e9fc-123">Os valores de hora local devem ser convertidos em valores de **Data** UTC.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="8e9fc-124">Atividades que o método **GetActivitiesEx** retorna devem ter um valor de tempo de criação que for maior do que _startTime_ e menor ou igual a **agora**.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="8e9fc-125">Se nenhuma alteração ocorreu entre **startTime** e **agora**, o provedor deve retornar um erro OSC_E_NO_CHANGES.</span><span class="sxs-lookup"><span data-stu-id="8e9fc-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e9fc-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e9fc-126">See also</span></span>

- [<span data-ttu-id="8e9fc-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e9fc-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="8e9fc-128">Sincronização de amigos e atividades</span><span class="sxs-lookup"><span data-stu-id="8e9fc-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

