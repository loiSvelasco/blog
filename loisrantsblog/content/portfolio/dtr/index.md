---
title: "Daily Time Record"
description: "An enhanced daily time recording system for my workplace"
---

{{< alert "github" >}}
You can view the entire code on my [GitHub](https://github.com/loiSvelasco/flask-sdoin-dtr)
{{< /alert >}}

This project details is still being written and it is still unfinished.
## Enhanced Daily Time Record for SDOIN


This project improves upon the existing generation of CSC Form 48 of the Schools Division of Ilocos Norte.

### Problems identified with the old system

- Year errors, the DTR was unable to work properly after the first year on production.
- Printing of CSC Form 48 is not consistent and often hard to print.
- Generating records does not work, in connection to the previous problem, records for the previous month is overwritten by newer data; which makes it hard for employees to generate their DTR for previous months.

### Solutions to the problems identified

- Year errors are no longer an issue, and an added benefit is the scalability of this project, with minimal to no maintenance needed.
- Printing of CSC Form 48 is improved and can now print two copies with a single sheet of A4 paper.
- Generating previous records is now possible and easier rather than having to select which year, month, etc. All the user needs to do is input his/her employee #, and the system automatically provides the months and years that has data.

## License
{{< alert "circle-info" >}}
This project is licensed under the [MIT License](https://github.com/loiSvelasco/flask-sdoin-dtr/blob/master/LICENSE)
{{< /alert >}}