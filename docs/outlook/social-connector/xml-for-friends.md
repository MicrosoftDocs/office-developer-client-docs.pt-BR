---
title: XML para amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: O elemento de amigos no esquema XML de provedor do Microsoft Outlook Social Connector (OSC) permite que um provedor OSC especificar informações para uma lista de pessoas associado a um usuário do Outlook na rede social.
ms.openlocfilehash: 07f1bb77e7912e3973fd2af8a70275642b72039c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770977"
---
# <a name="xml-for-friends"></a>XML para amigos

O elemento de **amigos** no esquema XML de provedor do Microsoft Outlook Social Connector (OSC) permite que um provedor OSC especificar informações para uma lista de pessoas associado a um usuário do Outlook na rede social. Se o provedor do OSC suporta a sincronização de cache, esta lista da pessoa conterá apenas amigos do usuário do Outlook na rede social. Se o OSC suporta a sincronização sob demanda ou híbrida, esta lista pode conter amigos e amigos do usuário do Outlook. 

Cada pessoa na lista é representada como um elemento da **pessoa** no esquema XML, que suporta detalhes como nome, sobrenome e endereços de email. Provedores OSC usam os elementos de **amigos** e a **pessoa** independentemente de como querem que o OSC sincronize as informações de amigo da rede social. Observe que os elementos filho de **pessoa** são similares a algumas das propriedades de um contato do Outlook, que facilita a amigos armazenando em uma pasta de contatos do Outlook específico à rede social, se suporta as redes sociais armazenado em cache ou híbrida sincronização de amigos a uma pasta de contatos do Outlook. 

## <a name="example-scenarios"></a>Cenários de exemplo

Os cenários de exemplo a seguir mostram o provedor do OSC chamadas de API de extensibilidade que implementa um provedor OSC e faz com que o OSC para obter informações de amigo. Informações é expresso em cadeias de caracteres XML que estão em conformidade com o esquema XML de provedor do OSC.
  
Para obter um exemplo de amigos XML, consulte [Exemplo de XML de amigos](friends-xml-example.md). Para obter mais informações sobre a sincronização de informações dos amigos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Cenário 1: Obtenha uma lista de amigos

Cenário 1 — OSC obtém uma lista de amigos e um objeto [ISocialPerson](isocialpersoniunknown.md) e uma imagem para cada amigo: 
    
1. Um provedor OSC que suporta mostrando amigos a partir do site de rede social e permitindo que o OSC informações do cache amigo indica que o OSC usando os elementos **getFriends** e **cacheFriends** , que são elementos filho do ** recursos** elemento. 
    
2. O provedor do OSC também implementa o [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e [ISocialPerson::GetPicture](isocialperson-getpicture.md) métodos. 
    
3. O OSC chama **ISocialProvider::GetCapabilities** para verificar o valor dos seguintes elementos: **getFriends** para verificar se o provedor OSC oferece suporte à mostrando amigos na rede social e **cacheFriends** para verificar se o provedor suporta o armazenamento em cache amigos. 
    
4. O OSC chama **ISocialSession::GetPerson** para obter um objeto **ISocialPerson** para o usuário do Outlook. 
    
5. O OSC chama **ISocialPerson::GetFriendsAndColleagues** para obter o usuário do Outlook da lista de amigos retornada na cadeia de caracteres de parâmetro _personCollection_ . A cadeia de caracteres _personCollection_ é compatível com a definição de esquema XML para o elemento de **amigos** no esquema XML. 
    
6. Para cada amigo na cadeia de caracteres XML _personCollection_ , o OSC obtém o valor do elemento **userID** chamar **ISocialSession::GetPerson** para obter um objeto **ISocialPerson** desse amigo. 
    
7. Para cada amigo na cadeia de caracteres XML **personCollection** , o OSC chama [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obter um recurso de imagem para desse amigo. 
    
   O OSC poderá fazer mais chamadas no objeto **ISocialPerson** para obter detalhes (por exemplo, endereços de email) e atividades desse amigo. 
    
### <a name="scenario-2-synchronize-friends"></a>Cenário 2: sincronizar amigos 

Cenário 2 — OSC sincroniza amigos dinamicamente:
    
1. Um provedor OSC que ofereça suporte a sincronização sob demanda de amigos e não-amigos indica que o OSC usando os elementos **getFriends** e **dynamicContactsLookup** . O provedor do OSC também define o elemento **hashFunction** . Todos os três elementos são elementos filho de **recursos**. 
    
2. O provedor do OSC também implementa o método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . 
    
3. O OSC chama **ISocialProvider::GetCapabilities** para verificar os valores de **getFriends** e **dynamicContactsLookup** para verificar se o provedor do OSC suporta amigos e a sincronização sob demanda de amigos e não-amigos. O OSC também torna Observação do valor do **hashFunction** suportada pelo provedor do OSC. 
    
4. Para cada usuário exibido no painel de pessoas, o OSC coleta o endereço de email do usuário e os criptografa usando a função de hash especificada em **hashFunction**. Isso forma uma sequência de caracteres XML que está em conformidade com a definição de esquema XML para o elemento **hashedAddresses** . 
    
5. O OSC chama **ISocialSession2::GetPeopleDetails**, fornecendo essa cadeia de caracteres XML de endereços com hash como o parâmetro _personAddresses_ , para obter dinamicamente detalhes atualizados para as pessoas no parâmetro _personsCollection_ . A cadeia de caracteres do parâmetro _personsCollection_ é compatível com a definição de esquema XML para o elemento de **amigos** no esquema XML. 

## <a name="parent-and-child-elements"></a>Elementos pai e filho

A seguir estão os dois elementos de nível superior no esquema de **amigos** . 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**amigos** <br/> |Representa o elemento raiz de uma lista dos elementos da **pessoa** . O **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)e **ISocialSession2::GetPeopleDetails** retornam cadeias de caracteres XML que estão em conformidade com a definição de esquema do elemento **amigos** .  <br/> |
|**person** <br/> |Representa uma pessoa em uma lista de elementos de **pessoa** . O método [ISocialPerson::GetDetails](isocialperson-getdetails.md) retorna uma sequência de caracteres XML que está em conformidade com a definição de esquema do elemento de **pessoa** .  <br/> |
   
A tabela a seguir descreve cada elemento filho do elemento **pessoa** no esquema XML de provedor do OSC. 
  
Para uma definição completa do esquema de XML de provedor OSC, incluindo quais elementos são obrigatórias ou opcionais, consulte [Esquema de XML para Outlook Social Connector Provider](outlook-social-connector-provider-xml-schema.md).
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**endereço** <br/> |Físico endereço da pessoa.  <br/> |
|**data especial** <br/> |Data de vencimento para um evento para a pessoa.  <br/> |
|**askmeabout** <br/> |Tópicos de interesse ou experiência da pessoa.  <br/> |
|**Aniversário** <br/> |Data de nascimento da pessoa.  <br/> |
|**businessAddress** <br/> |Endereço de rua físico do local de trabalho da pessoa.  <br/> |
|**Cidade do endereço comercial** <br/> |Cidade do local de trabalho da pessoa.  <br/> |
|**businessCountryOrRegion** <br/> |País ou região do local de trabalho da pessoa.  <br/> |
|**businessState** <br/> |Estado ou província do local de trabalho da pessoa.  <br/> |
|**businessZip** <br/> |CEP ou código postal do local de trabalho da pessoa.  <br/> |
|**célula** <br/> |Número de telefone celular da pessoa.  <br/> |
|**Cidade** <br/> |Cidade do endereço físico para a pessoa.  <br/> |
|**empresa** <br/> |Nome da empresa associada com a pessoa.  <br/> |
|**countryOrRegion** <br/> |País ou região do endereço da pessoa físico.  <br/> |
|**creationTime** <br/> |Hora da criação do perfil da pessoa na rede social.  <br/> |
|**emailAddress** <br/> |Endereço de email primário da pessoa.  <br/> |
|**emailAddress2** <br/> |Endereço de email secundário da pessoa.  <br/> |
|**emailAddress3** <br/> |Endereço de email terciário da pessoa.  <br/> |
|**expirationTime** <br/> |Hora em que os dados de perfil da pessoa expirem na rede social.  <br/> |
|**fileAs** <br/> |Cadeia de caracteres pelo qual a pessoa deve ser arquivado como arquivo de contatos de um contato no Outlook.  <br/> |
|**firstName** <br/> |Nome ou o nome da pessoa.  <br/> |
|**friendStatus** <br/> |Status de amigo desta pessoa com o usuário conectado na rede social. Deve ser um dos seguintes valores: **amigo**, **nonfriend**, **pendente**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Nome completo da pessoa.  <br/> |
|**Gênero** <br/> |Gênero da pessoa. Deve ser um dos seguintes valores: **Masculino**, **Feminino**, **não especificada**.  <br/> |
|**homePhone** <br/> |Número de telefone residencial para a pessoa.  <br/> |
|**índice** <br/> |Local do endereço da pessoa com hash no parâmetro _personsAddresses_ cadeia de caracteres passada para uma chamada ao método **ISocialSession2::GetPeopleDetails** . Ele também indica **pessoa** XML na cadeia de caracteres _personsCollection_ retornada por **GetPeopleDetails da pessoa**.  <br/> |
|**setores** <br/> |Setores que a pessoa está envolvida em.  <br/> |
|**interests** <br/> |Interesses ou hobbies da pessoa.  <br/> |
|**lastModificationTime** <br/> |Hora em que o perfil da pessoa da última modificação na rede social.  <br/> |
|**lastName** <br/> |Último nome ou sobrenome da pessoa.  <br/> |
|**location** <br/> |O local da pessoa.  <br/> |
|**Apelido** <br/> |Um nome mais curto ou fictício nome da pessoa.  <br/> |
|**otherAddress** <br/> |Alternativo endereço da pessoa.  <br/> |
|**otherCity** <br/> |Cidade do endereço de alternativo da pessoa.  <br/> |
|**otherCountryOrRegion** <br/> |País ou região do endereço de alternativo da pessoa.  <br/> |
|**otherState** <br/> |Estado ou província do endereço de alternativo da pessoa.  <br/> |
|**otherZip** <br/> |CEP ou código postal do endereço de alternativo da pessoa.  <br/> |
|**telefone** <br/> |Número de telefone do contato principal para a pessoa.  <br/> |
|**pictureUrl** <br/> |URL para uma imagem de perfil da pessoa.  <br/> |
|**relacionamento** <br/> |Relação entre essa pessoa com o usuário conectado.  <br/> |
|**escolas** <br/> |As instituições de ensino que a pessoa entra ou fui.  <br/> |
|**skills** <br/> |Habilidades pessoais da pessoa.  <br/> |
|**state** <br/> |Estado ou província do endereço físico da pessoa.  <br/> |
|**title** <br/> |Indicação adicionada ao nome da pessoa.  <br/> |
|**userID** <br/> |ID para identificar a pessoa na rede social.  <br/> |
|**webProfilePage** <br/> |Endereço da página da Web que contém um perfil da pessoa.  <br/> |
|**site da Web** <br/> |Site da pessoa.  <br/> |
|**workPhone** <br/> |Número do telefone comercial para a pessoa.  <br/> |
|**ZIP** <br/> |CEP ou código postal do endereço físico da pessoa.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Exemplo de XML de amigos](friends-xml-example.md)  
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para recursos](xml-for-capabilities.md) 
- [XML para atividades](xml-for-activities.md)
- [Desenvolvendo um provedor com o esquema OSC XML](developing-a-provider-with-the-osc-xml-schema.md)

