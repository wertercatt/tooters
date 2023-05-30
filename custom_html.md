/*
    * Shrink the font size a smidge for post content
    * Indent the paragraph text
    * Stop posts from getting too tall by capping content 
      height, and adding scrollbar if exceeded
        - 350px seems to be the sweet spot - maybe 90% of 
          posts don’t hit the height cap
    * This alignment intentionally does not apply to
      expanded posts.
*/
.status .reply-indicator__content, .status .status__content {
    margin-left: calc(58px - 0.5em);
    font-size: 1.075em;
    padding: 0 0.5em;
    max-height: 350px;
    overflow-y: auto;
}

/*
    * Narrow the media icon on status cards, so that the
      card title aligns with post content
*/
.status-card.compact .status-card__image {
    flex: 0 0 calc(58px - 0.75em);
}

/*
    * Brighten the post privacy indicator a tad if public but
      not listed in public timelines
    * Set a bright color for privacy indicator if locked to
      followers or specific recipients
*/
.status__visibility-icon .fa-lock, 
.status__visibility-icon .fa-at {
    color: #FF6BAF;
}
.status__visibility-icon .fa-unlock {
    color: #018674;
}

/*
    * Give avatar photos a fun rounded blob shape
    * Profile page photos are still rounded squares
*/
.account__avatar {
    border-bottom-left-radius: 50%;
    border-bottom-right-radius: 50%;
    border-top-left-radius: 70%;
    border-top-right-radius: 70%;
}
.account__header__tabs .account__avatar {
    border-radius: 4px;
}

.compose-form__publish-button-wrapper button, .button[href = “/publish”] {
  text-indent: -9999px;
  line-height: 0; /* Collapse the original line */
}

.compose-form__publish-button-wrapper button:after, .button[href = “/publish”]:after {
  content:’Toot’; 
  text-indent: 0;
  display: block;
  line-height: initial; /* New content takes up original line height */
}

.status-direct {
background: rgba(0,0,0,.1);
box-shadow: inset 0 0 0 2px rgba(0, 0, 0, 40%);
}