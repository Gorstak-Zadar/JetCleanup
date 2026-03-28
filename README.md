<!-- description: JetCleanup.reg: deletes hundreds of HKCU keys (classes, app events, personalization)—aggressive profile trim; backup before merge. -->

# JetCleanup

**`JetCleanup.reg`** is a **registry merge** that **deletes** (`[-HKEY_...]`) a **long** list of **`HKEY_CURRENT_USER`** keys—covering **AppEvents** sound schemes, **Control Panel** branches (Bluetooth, personalization, quick actions, …), **file class registrations** (**.amr**, **.divx**, …), vendor keys (**AMD**, …), and many more.

**Intent:** strip “bloat” or reset parts of the **per-user** profile (the name suggests a **leaner** shell experience).

**Risks:** Removing **ProgID** / **file association** keys can **break** double-click behavior for those extensions. **Export HKCU** or create a **restore point** before **`reg import`**. Review the file in chunks—it is **large** (800+ lines of deletes).

---

## Usage

```cmd
reg import JetCleanup.reg
```

Test on a **throwaway** Windows user first.

---

## Disclaimer

**NO WARRANTY.** THERE IS NO WARRANTY FOR THE PROGRAM, TO THE EXTENT PERMITTED BY APPLICABLE LAW. EXCEPT WHEN OTHERWISE STATED IN WRITING THE COPYRIGHT HOLDERS AND/OR OTHER PARTIES PROVIDE THE PROGRAM "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE ENTIRE RISK AS TO THE QUALITY AND PERFORMANCE OF THE PROGRAM IS WITH YOU. SHOULD THE PROGRAM PROVE DEFECTIVE, YOU ASSUME THE COST OF ALL NECESSARY SERVICING, REPAIR OR CORRECTION.

**Limitation of Liability.** IN NO EVENT UNLESS REQUIRED BY APPLICABLE LAW OR AGREED TO IN WRITING WILL ANY COPYRIGHT HOLDER, OR ANY OTHER PARTY WHO MODIFIES AND/OR CONVEYS THE PROGRAM AS PERMITTED ABOVE, BE LIABLE TO YOU FOR DAMAGES, INCLUDING ANY GENERAL, SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OR INABILITY TO USE THE PROGRAM (INCLUDING BUT NOT LIMITED TO LOSS OF DATA OR DATA BEING RENDERED INACCURATE OR LOSSES SUSTAINED BY YOU OR THIRD PARTIES OR A FAILURE OF THE PROGRAM TO OPERATE WITH ANY OTHER PROGRAMS), EVEN IF SUCH HOLDER OR OTHER PARTY HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

---

## Disclaimer (read this; it matters)

This software and documentation are provided **“as is”**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. **Use at your own risk.**

If you do not agree, **do not use** this repository.
