[MODEL DESIGN]


from django.db import models
from ckeditor.fields import RichTextField

class FAQ(models.Model):
    question_en = models.TextField()  # English question
    question_hi = models.TextField(blank=True, null=True)  # Hindi translation
    question_bn = models.TextField(blank=True, null=True)  # Bengali translation
    answer = RichTextField()  # WYSIWYG formatted answer

    def get_translated_question(self, lang='en'):
        """Retrieve translated question dynamically."""
        return getattr(self, f'question_{lang}', self.question_en) or self.question_en

    def __str__(self):
        return self.question_en

[INSTALL DJANGO]
pip install django-ckeditor

[Add it to INSTALLED_APPS and configure it in settings.py]

INSTALLED_APPS = [
    'ckeditor',
    'faq',  # Your app name




