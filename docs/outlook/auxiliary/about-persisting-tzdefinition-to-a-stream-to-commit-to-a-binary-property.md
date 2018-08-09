---
title: Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: As propriedades de fuso horário, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur e PidLidAppointmentTimeZoneDefinitionStartDisplay são binário denominado propriedades, cada um deles contém um stream que mapeie para o formato persistente de uma estrutura TZDEFINITION.
ms.openlocfilehash: 8e00c7203e2a0adfdf9ff3e6dadff6485c8b5111
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765786"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a><span data-ttu-id="9e113-103">Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária</span><span class="sxs-lookup"><span data-stu-id="9e113-103">About persisting TZDEFINITION to a stream to commit to a binary property</span></span>

<span data-ttu-id="9e113-104">As propriedades de fuso horário, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)e [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) são binário denominado propriedades, cada um deles contém um stream que mapeie para o formato persistente de uma estrutura [TZDEFINITION](tzdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="9e113-104">The time zone properties, [PidLidAppointmentTimeZoneDefinitionEndDisplay](http://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](http://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx), and [PidLidAppointmentTimeZoneDefinitionStartDisplay](http://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) are binary named properties, each of which contains a stream that maps to the persisted format of a [TZDEFINITION](tzdefinition.md) structure.</span></span> 
  
<span data-ttu-id="9e113-105">Este tópico descreve um pouco formato endian que pode ser usado quando mantendo **TZDEFINITION** a um fluxo para comprometer a uma das três propriedades binárias.</span><span class="sxs-lookup"><span data-stu-id="9e113-105">This topic describes a little endian format that can be used when persisting **TZDEFINITION** to a stream to commit to one of three binary properties.</span></span> <span data-ttu-id="9e113-106">Use o mesmo formato endian em um analisador para interpretar um valor de stream obtido de uma dessas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e113-106">Use the same endian format in a parser to interpret a stream value obtained from one of these properties.</span></span> 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

<span data-ttu-id="9e113-107">O número de versão principal é usado para fazer uma quebra de alteração.</span><span class="sxs-lookup"><span data-stu-id="9e113-107">The major version number is used to make a breaking change.</span></span> <span data-ttu-id="9e113-108">Clientes que não estiver familiarizados com o número da versão principal devem tratar a propriedade como se ele não estiver lá.</span><span class="sxs-lookup"><span data-stu-id="9e113-108">Clients that are unfamiliar with the major version number should treat the property as if it is not there.</span></span> <span data-ttu-id="9e113-109">Gravando a estrutura de clientes devem especificar a constante **TZ_BIN_VERSION_MAJOR**.</span><span class="sxs-lookup"><span data-stu-id="9e113-109">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MAJOR**.</span></span> 
  
<span data-ttu-id="9e113-110">O número da versão secundária é usado para fornecer extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="9e113-110">The minor version number is used for extensibility.</span></span> <span data-ttu-id="9e113-111">Clientes que não estiver familiarizados com o número da versão secundária devem ler os dados que eles entender e ignoram os dados que podem ser acrescentados para cada regra ou para o fluxo geral.</span><span class="sxs-lookup"><span data-stu-id="9e113-111">Clients that are unfamiliar with the minor version number should read the data that they understand, and skip over the data that might be appended to each rule or to the overall stream.</span></span> <span data-ttu-id="9e113-112">Gravando a estrutura de clientes devem especificar a constante **TZ_BIN_VERSION_MINOR**.</span><span class="sxs-lookup"><span data-stu-id="9e113-112">Clients writing the structure should specify the constant **TZ_BIN_VERSION_MINOR**.</span></span> 
  
<span data-ttu-id="9e113-113">Se um analisador não entender a versão principal do cabeçalho, ela não deve ler o restante da estrutura e se comportam como se os dados estão ausentes.</span><span class="sxs-lookup"><span data-stu-id="9e113-113">If a parser does not understand the major version of the header, it should not read the rest of the structure and behave as if the data is missing.</span></span> <span data-ttu-id="9e113-114">Se um analisador não entender a versão secundária do cabeçalho, ele deve usar **cbHeader** para ignorar as partes que ele não entende e avanço para ler as partes do stream que ela compreende.</span><span class="sxs-lookup"><span data-stu-id="9e113-114">If a parser does not understand the minor version of the header, it should use **cbHeader** to ignore the portions that it does not understand and advance to read the portions of the stream that it understands.</span></span> 
  
<span data-ttu-id="9e113-115">O valor de **wFlags** é sempre **TZDEFINITION_FLAG_VALID_KEYNAME**.</span><span class="sxs-lookup"><span data-stu-id="9e113-115">The value of **wFlags** is always **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span> <span data-ttu-id="9e113-116">O nome da chave tem um tamanho máximo de **MAX_PATH**.</span><span class="sxs-lookup"><span data-stu-id="9e113-116">The key name has a maximum size of **MAX_PATH**.</span></span> 
  
<span data-ttu-id="9e113-117">Se um analisador não reconhece a versão principal de uma regra, o cliente deve ignorar a regra e use **cbRule** para ir para a próxima regra.</span><span class="sxs-lookup"><span data-stu-id="9e113-117">If a parser does not recognize the major version of a rule, the client should ignore the rule, and use **cbRule** to advance to the next rule.</span></span> <span data-ttu-id="9e113-118">Se um analisador não reconhece a versão secundária de uma regra, o cliente só deve analisar as partes da regra que ela compreende.</span><span class="sxs-lookup"><span data-stu-id="9e113-118">If a parser does not recognize the minor version of a rule, the client should only parse the parts of the rule that it understands.</span></span> 
  
<span data-ttu-id="9e113-119">Quando mantendo uma estrutura **TZDEFINITION** a um fluxo, um analisador não deve tentar gravar todas as informações que ele não entende.</span><span class="sxs-lookup"><span data-stu-id="9e113-119">When persisting a **TZDEFINITION** structure to a stream, a parser should not try to write any information that it does not understand.</span></span> 
  
<span data-ttu-id="9e113-120">O número máximo de regras é 1024.</span><span class="sxs-lookup"><span data-stu-id="9e113-120">The maximum number of rules is 1024.</span></span>
  
<span data-ttu-id="9e113-121">Observe que a estrutura [TZREG](tzreg.md) é persistente aqui diferentemente vez quando persistentes sozinhos, portanto o mesmo código não pode ser usado para analisá-lo.</span><span class="sxs-lookup"><span data-stu-id="9e113-121">Note that the [TZREG](tzreg.md) structure is persisted here differently than when persisted alone, so the same code cannot be used to parse it.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9e113-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e113-122">See also</span></span>

- [<span data-ttu-id="9e113-123">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="9e113-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="9e113-124">Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="9e113-124">Parse a stream from a binary property to read the TZDEFINITION structure</span></span>](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [<span data-ttu-id="9e113-125">Ler propriedades de fuso horário de um compromisso</span><span class="sxs-lookup"><span data-stu-id="9e113-125">Read time zone properties from an appointment</span></span>](how-to-read-time-zone-properties-from-an-appointment.md)

