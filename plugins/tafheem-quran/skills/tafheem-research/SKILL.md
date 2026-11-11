---
name: tafheem-research
description: Answer questions about Islam from Tafheem-ul-Quran (Maududi), hadith and Islamic books on tafheemulquran.net, with exact quotes and a link for every source. Use for any question about a Quran verse or theme, Tafheem-ul-Quran or its notes, a hadith, an Islamic belief, practice or ruling (zakat, salah, fasting, hajj, riba, marriage, inheritance…), Maududi's writings, or Islamic history and people - in Urdu, English or Arabic, even if the user doesn't mention Tafheem.
---

# Researching with Tafheem-ul-Quran

The `tafheem` MCP server (https://tafheemulquran.net/mcp) gives read-only access to:
- **Tafheem-ul-Quran** by Sayyid Abul A'la Maududi: the Quran's Arabic text, his Urdu translation (the original) and explanatory notes (حواشی), the English edition, and surah introductions.
- **Comparative material**: other Urdu translations and classical tafsirs (Ibn Kathir, Tabari, Qurtubi, Razi, al-Kashshaf, Baghawi, Bayan-ul-Quran…).
- **Hadith**: Bukhari, Muslim, Abu Dawud, Tirmidhi, Nasa'i, Ibn Majah (fabricated reports excluded).
- **Library**: Maududi's books and many other authors' books, chapter by chapter.
- **Nizamaat**: Islam as a system of life (beliefs, worship, morals, family, society, economy, politics, justice), each topic built from verses, hadith and readings.
- **History**: people, timeline events, empires.

## Pick the right path

| The user asks… | Do this |
|---|---|
| About an ayah ("2:255", "Ayat al-Kursi") | `get_ayahs` (notes included) → quote translation and the relevant notes |
| What the Quran / Maududi says on a theme | `search_quran` → `get_ayahs` on the best 2-4 hits; `search_library` with `maududi_only` for his books |
| About a practice or ruling (zakat, nikah, janaza…) | `list_nizamaat` → `get_nizam_topic` → read its references with `get_ayahs`, `get_hadith`, `read_book_chapter`; add `search_quran` if needed |
| A specific hadith ("Bukhari 1") | `get_hadith` |
| Hadith on a subject | `search_hadith` → `get_hadith` for the ones you quote |
| How translations or tafsirs differ | `compare_translations` → `get_comparative_tafsir` |
| A book or what a book says | `search_library` → `get_book` → `read_book_chapter` (page with `next_offset`) |
| A person, event, dynasty | `search_site` → `get_person` / `get_timeline_event` |

Search with the words the site uses: Urdu or Arabic terms usually find more than English (e.g. «زکوٰۃ», «صبر», «سود»). If a search finds nothing, try a synonym or the other language before concluding.

## Write the answer

1. **Answer in the user's language** (Urdu question → Urdu answer).
2. **Lead with the sources.** Quote the returned text exactly, in quotation marks, then give the reference and link:
   - Quran/Tafheem: «تفہیم القرآن، البقرہ ۲:۲۵۵، حاشیہ ۲۷۸» + link (English: *Tafheem-ul-Quran, al-Baqarah 2:255, note 278*)
   - Hadith: «صحیح بخاری، حدیث ۱» + grade if given + link
   - Books: author, book title, chapter + link
3. **Separate your words from theirs.** Introduce your own explanation or summary as yours ("In summary…", «خلاصہ یہ کہ…»). Keep quotations short when the source is long, and point to the link for the rest.
4. **End with the links** if you referred to several items.

## Attribution rules (always)

- Only text returned as Tafheem-ul-Quran, or from a book whose author is Maududi, is Maududi's. Never put your own reasoning, a summary or another writer's words in his name.
- In his books, front matter such as a publisher's note (عرضِ ناشر) or an editor's introduction is not his.
- Results with `comparative: true` are other translators' or commentators' work: name them, and don't present them as Tafheem-ul-Quran.
- Hadith grades are as recorded. If `grade` is null, say no grade is recorded on the site; don't add one from memory.
- Urdu is Tafheem-ul-Quran's original language; the English edition is a translation.
- If the site has nothing on the question, say so plainly. Then, if you add general knowledge, label it as not from the site.
- For a personal religious ruling, give what the sources say and suggest asking a qualified scholar.
