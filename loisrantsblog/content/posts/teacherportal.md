+++
draft = false
date = 2022-10-13T19:59:43+08:00
title = "A system for teachers"
description = ""
slug = ""
tags = ["idea", "development", "programming"]
categories = []
externalLink = ""
+++

## Is it needed?

A colleague of mine approached me with an idea of a system that tracks all trainings and seminars an employee or staff attended; in this case, teachers. Since I work in the education sector of our government, they handle a lot of personal records; which then gave me the idea of a portal for teachers (and non-teaching staff too, maybe) much like a portal for students where they can see their grades, schedules, balances, etc. It will work the same but for different sets of data, i.e. trainings attended, to attend, past trainings offered, personal work records, work history, accomplishments, innovations, etc.

When thinking about it, these specific sets of records can and will help the selection process for teachers for promotion, even if this system is only accessible by our division, they will be able to extract the info they need and present it where they need it presented. Think of this as a digital copy of self and work related documents. To answer the question, yes; it is needed.


## What will be my approach?

A web-based approach fits this project perfectly. It enables access across devices, regardless of where you are, and this might even serve the whole region if built and maintained correctly. Which I hope I could, I work alone without a team so I'll do my best.


## Requirements?

For end-users, all that is needed is a computer or mobile phone, and a stable internet connection.
For the server, any server would do, with a large storage space for documents and photos or other media, and a host with near to unlimited bandwidth to accomodate traffic for the first few weeks of deployment (I'm speaking as if this will work, which as of now I have no way of knowing, but I'll keep things positive.)


## Initial flow (End-User)
{{< mermaid >}}
flowchart TB
    start([Start])-->acc{login}
    acc-- yes -->login(Login)
    acc-- no -->reg(Register)-->acc
    login-->menu{Menu}
    fallback(((M)))-->menu
    menu-->Settings
    menu-->Trainings
    menu-->Profile
    menu-->Logout-->logout(((D)))
    Settings-->user(((A)))
    Trainings-->trainings(((B)))
    Profile-->profile(((C)))
{{< /mermaid >}}

{{< mermaid >}}
flowchart LR
    user(((A)))-->settMenu{"&nbsp"}
    settMenu-->pass[Edit Pass]-->Save
    settMenu-->name[Edit Name]-->Save
    settMenu-->email[Edit Email]-->Save-->fallback(((M)))
{{< /mermaid >}}

{{< mermaid >}}
flowchart TD
    user(((B)))-->trainMenu{"&nbsp"}
    trainMenu-->Attended-->list0[Show List]
    trainMenu-->All-->list0[Show List]-->fallback(((M)))
    trainMenu-->Upcoming-->list1[Show List]-->attendyn{Attend?}
    attendyn--yes-->Save-->fallback(((M)))
    attendyn--no-->list1
{{< /mermaid >}}

{{< mermaid >}}
flowchart LR
    user(((C)))-->profMenu{"&nbsp"}
    profMenu-->por[Portfolio / Innovations]-->manp[Manage/Edit]
    profMenu-->exp[Work Experience]-->manp-->Save-->fallback(((M)))
{{< /mermaid >}}

{{< mermaid >}}
flowchart TD
    logout(((D)))-->finn([End])
{{< /mermaid >}}


## Initial flow (Admin)
{{< mermaid >}}
flowchart TD
    login-->menu{Menu}
    fallback(((M)))-->menu
    menu-->admUsers[Users]
    menu-->admTrain[Trainings]
    menu-->Profile
    menu-->Logout-->logout(((D)))
    admUsers-->dash[Generic Dashboard for Managing Data]
    admTrain-->manpTrain(((T)))
    Profile-->dash
{{< /mermaid >}}

{{< mermaid >}}
flowchart LR
    manpTrain(((T)))-->menu{"&nbsp"}
    menu-->edit[Edit Training]
    menu-->add[Add Training]
{{< /mermaid >}}